---
source-hash: d4fdeaa3f3d1430002a0e679e72ccee20fec335cb9d13974b60c5cadd82a094e
sidebar_position: 7
---

# Jak skompilować OsmAndMapCreator i narzędzia {#how-to-compile-osmandmapcreator-and-tools}


## Kompilacja OsmAndMapCreator {#compile-osmandmapcreator}
1. Najpierw skonfiguruj **[środowisko programistyczne](setup-the-dev-environment.md)**.
2. **Gradle** (wiersz poleceń):
    - Kompiluj z wiersza poleceń
    ```
    cd tools/java-tools && ../gradlew build
    ```
    - OsmAndMapCreator.zip zostanie wygenerowany ze wszystkimi skryptami w środku
    **Uwaga**: projekt Android jest wymagany do zbudowania narzędzi (używa projektu OsmAnd-java).
3. **Eclipse**:
    - Wstępnie skonfiguruj projekty Eclipse
    ```
    cd tools/java-tools && ../gradlew cleanEclipse eclipse
    ```
    - W Eclipse 'Import' - 'Existing projects in workspace' wybierz foldery 'OsmAnd-java', 'OsmAndMapCreatorutilities', 'OsmAndMapCreator', 'OsmAndServer', 'OsmAndServerUtilties'.
    **Uwaga**: nie wybieraj głównego folderu java-tools, zamiast tego wybierz projekty wymienione powyżej.
4. Android Studio / Idea
    Zachęcamy do przesłania pull requesta do tej dokumentacji i opisania, jak to zrobić.
5. Główne klasy do wykonania z IDE:
   - net.osmand.MainUtilities - reprezentuje utilities.sh i prowadzi do wszystkich możliwych narzędzi.
   - net.osmand.obf.BinaryInspector - narzędzie inspector.sh do odczytu plików OBF i dostarczania informacji o nich.
   - net.osmand.obf.preparation.IndexCreator - skrót do generowania pliku obf.
   - net.osmand.swing.OsmExtractionUI - OsmAndMapCreator

## Kompilacja natywnej biblioteki renderującej dla OsmAndMapCreator {#compile-native-rendering-library-for-osmandmapcreator}
Natywna biblioteka renderująca może być używana do testowania renderowania offline lub natywnego routingu offline. Jest to bardzo przydatne do debugowania i testowania stylu renderowania lub konfiguracji routingu.

1. Najpierw skonfiguruj **środowisko programistyczne**, zobacz [środowisko programistyczne](./setup-the-dev-environment).
2. Pobierz zewnętrzne zależności
 ```
 cd core-legacy/externals
 ./configure.sh
 ```
3. Określ JAVA_HOME globalnie za pomocą $PATH lub w wierszu poleceń
  ```
  export JAVA_HOME=<>
  ```
4. Wybierz konkretny [cel](https://github.com/osmandapp/OsmAnd-core/tree/legacy_core/targets) dla systemu operacyjnego i skompiluj konkretną wersję 'debug', 'release' lub '' (domyślnie). Przykład
  ```
  cd core-legacy/targets
  ./intel-darwin.sh release # macOs release
  ./amd64-linux-clang.sh debug # linux debug - default
  cd ....baked # np. intel-darwin-intel-darwin-clang-release.baked lub amd64-linux-amd64-clang-release.baked
  make -j4
  ```
5. Pliki binarne będą dostępne w core-legacy/binaries/.
Przykład:
  ```
    core-legacy/binaries/darwin/intel/Debug/libosmand.dylib
  ```

### Rozwiązywanie problemów {#troubleshooting}
- Brakujące pliki externals/libjpeg-turbo/jconfigint.h.in nie istnieją.
Jeśli doświadczasz, że libjpeg-turbo nie mógł się skompilować
```
targets/.cmake/../../externals/skia/upstream.patched/third_party/externals/libjpeg-turbo/jconfigint.h.in does not exist.
```
Możesz znaleźć pliki tutaj i umieścić je w określonym folderze
https://github.com/osmandapp/OsmAnd-core/blob/legacy_core/externals/jpeg/jconfig.h
https://github.com/osmandapp/OsmAnd-core/blob/legacy_core/externals/jpeg/jconfigint.h

## Kompilacja wersji qt core dla OsmAndMapCreator {#compile-qt-core-version-for-osmandmapcreator}
1. Najpierw skonfiguruj **[środowisko programistyczne](setup-the-dev-environment.md)**.
2. Przygotuj kompilację (cmake) dla konkretnego celu. Przykład clang / linux:
```
   alias clang='clang -std=c++11'
   build/amd64-linux-clang.sh release
```
3. Kompiluj bibliotekę release
```
    (cd "baked/amd64-linux-clang-release.make" && make -j4)
```