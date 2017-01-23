## Install OpenCV-Java into Mac
### In terminal
1. Install Homebrew-Science (once)
>$brew tap homebrew/science

2. Install OpenCV
>$brew install opencv3 --with-java

3. Into file
>$cd usr/local/Cellar/opencv3/3.1.0_4/share/java

### Eclipse
1. [Terminal] Copy or rename file
>$cp ./libopencv_java310.so libopencv_java310.dylib

2. [Eclipse] eclipse -> preference ->Java -> Build Path -> User Libraries

3. Press "New"

4. Input library name "opencv-(version)"

5. Click library you made

6. Click "Add External JARs..." -> add "opencv-310.jar"

7. Expand "opencv-3.1" -> "Native library location" -> "External Folder..." -> "libopencv_java310.dylib"

8. In your project, Build Path -> Add libraries... -> user library & Next -> check "opencv-3.1"

### Intelli J
1. [Intelli J] File -> Project Structure... -> Libraries
  ->"+" -> Java

2. Select "/usr/local/Cellar/opencv3/3.1.0_4/share/OpenCV/java/opencv-310.jar"

3. "projectName" -> Edit Configurations
  ->Confuguration -> Input "-Djava.library.path=/usr/local/Cellar/opencv3/3.1.0_4/share/OpenCV/java" in "VM options"
