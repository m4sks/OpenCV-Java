## Install OpenCV-Java into Mac
### In terminal
$brew tap homebrew/science   (homebrew/scienceのinstall, 以前に行っていれば必要なし)

$brew install opencv3 --with-java   (openCVのversionによりopencv(version上1桁))

$cd usr/local/Cellar/opencv3/3.1.0_4/share/java    //installしたdirectriの(version)/share/OpenCV/javaに入る

### eclipse
$mv libopencv_java310.so をlibopencv_java310.dylibに書き換え(コピーして書き換えをお勧めする)

eclipse -> preference

Java -> Build Path -> User Libraries

Press "New"

Input library name "opencv-3.1"

Press library you made

Press "Add External JARs..." -> add "opencv-310.jar"

Expand "opencv-3.1" -> Press "Native library location" -> Press "External Folder..." -> Double click "libopencv_java310.dylib"

使いたいProjectで右クリックしてBuild Path -> Add libraries... -> user library & Next -> check "opencv-3.1". Finish.

### Intelli J
File -> Project Structure... -> Libraries 
  ->左上の "+" -> Java -> Select /usr/local/Cellar/opencv3/3.1.0_4/share/OpenCV/java/opencv-310.jar -> ok

右上の"projectName"を押す -> Edit Configurations
  ->Confuguration -> VM optionsに-Djava.library.path=/usr/local/Cellar/opencv3/3.1.0_4/share/OpenCV/javaを入れる

(/usr/local/Cellar/opencv3/3.1.0_4/share/OpenCV/java/の.soファイルをeclipse用に書き換えてしまっていたら,
  .soに書き換えコピー($cp /usr/local/Cellar/opencv3/3.1.0_4/share/OpenCV/java/libopencv_java310.dylib libopencv_java310.dylib))
