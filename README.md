<p align="center">
<a href="https://bimalka98.github.io/">
<img width="100px" src="https://github.com/bimalka98/bimalka98/blob/master/Logos/b98-logo.png" align="center"/>
</a>

<!--
### *Add Anaconda Prompt to the Windows right click context menu.*

1. Run regedit.exe (or type "Registry Editor" in windows search)
2. Navigate to `HKEY_CLASSES_ROOT > Directory > Background > shell`
3. Right click on the shell folder and add a new key named `AnacondaPrompt` and set its value to "Anaconda Prompt Here" (or anything you'd like it to appear as in the right click context menu)
4. Add a new key under this key, called `command`, and set its value to `cmd.exe /K C:\Users\ASUS\Anaconda3\Scripts\activate.bat` (may have to change the activate.bat file to where ever Anaconda is installed)
5. Go to the folder you want, right click and click "Anaconda Prompt Here".
6. That's it.
-->

<h2 align="center"> Contents❄ </h2>

1. [Creating a virtual environment for Computer Vision](#creating-a-virtual-environment-for-computer-vision)
2. [Editor Configurations](#editor-configurations)
3. [Applications](#applications)
4. [References](#references-)

---

# *Creating a virtual environment for Computer Vision*

Complete guide can be found [here](https://youtu.be/xE8w6OQzf8w)

Following steps describe only the creation of virtual environments.

1. Open command Prompt and follow the steps.

2. Change the Directory to: `C:\Python39`

3. Upgrade pip: `python -m pip install --upgrade pip`

4. Install `virtualenv` package: `python -m pip install virtualenv`

5. Create virtual environment: `virtualenv cv`

6. Activate the cv environment: `C:\Python39\cv\Scripts>activate`

7. Then install the required packages

```
pip install numpy
pip install matplotlib
pip install opencv-python
pip install jupyterlab
```



# *Editor Configurations*

## *Using Jupyter Lab*

Environment created above can be activated in any folder through `GIT Bash` using the following commands.

```
$ source /c/Python39/cv/Scripts/activate
$ jupyter lab
```

## *Using Visual Studio Code*

### Extensions to be installed

* Jupyter Extension for Visual Studio Code
* TabNine Autocomplete AI: JavaScript, Python, TypeScript, PHP, C/C++, HTML/CSS, Go, Java, Ruby, C#, Rust, SQL, Bash, Kotlin, Julia, Lua, OCaml, Perl, Haskell, React

---
# *Applications*

|Figure|Desciption|
|:---:|:---|
|<img src="https://github.com/bimalka98/Computer-Vision-and-Image-Processing/blob/main/Applications/Smoothed%20Sobel%20gradient%20and%20Laplacian%20for%20greater%20Sharpening.png"  width="800" />|[Smoothed Sobel gradient and Laplacian for greater Sharpening](https://github.com/bimalka98/Computer-Vision-and-Image-Processing/blob/main/Applications/Smoothed%20Sobel%20gradient%20and%20Laplacian%20for%20greater%20Sharpening.ipynb) [Original Image source](http://gamma.wustl.edu/bs044te241.html)|


---
## *References* 📌

1. [Fundamentals of Image Processing and Computer Vision](https://youtube.com/playlist?list=PLELEBz6g6MJanTKBAUJni8FTa8FC8gqGP) On Youtube by [*Dr Ranga Rodrigo*](http://ranga.staff.uom.lk/)

2. Digital Image Processing(Third Edition) by *Rafael C. Gonzalez* and *Richard E. Woods*
