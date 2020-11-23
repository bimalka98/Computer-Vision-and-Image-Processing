## Computer Vision and Image Processing

Computer Vision and Image Processing algorithms implemented using OpenCV, NumPy and MatPlotLib, for UOM's EN2550 Fundamentals of Image Processing and Machine Vision Module ❄

<!--
### *Add Anaconda Prompt to the Windows right click context menu.*

1. Run regedit.exe (or type "Registry Editor" in windows search)
2. Navigate to `HKEY_CLASSES_ROOT > Directory > Background > shell`
3. Right click on the shell folder and add a new key named `AnacondaPrompt` and set its value to "Anaconda Prompt Here" (or anything you'd like it to appear as in the right click context menu)
4. Add a new key under this key, called `command`, and set its value to `cmd.exe /K C:\Users\ASUS\Anaconda3\Scripts\activate.bat` (may have to change the activate.bat file to where ever Anaconda is installed)
5. Go to the folder you want, right click and click "Anaconda Prompt Here".
6. That's it.
-->

### *Creating a virtual environment for Computer Vision*

Complete guide can be found [here](https://youtu.be/xE8w6OQzf8w)

Following steps describe only the creation of virtual environments.

1. Open command Prompt and follow the steps.

2. Change the Directory to `C:\Python39`

3. Upgrade pip `python -m pip install --upgrade pip`

4. Install `virtualenv` package `python -m pip install virtualenv`

5. Create virtual environment `virtualenv cv`

6. Activate the cv environment `C:\Python39\cv\Scripts>activate`

7. Then install the required packages

```
pip install numpy
pip install matplotlib
pip install opencv-python
pip install jupyterlab
```

This environment can be activated in any folder through `GIT Bash` using the following commands.

```
$ source /c/Python39/cv/Scripts/activate
$ jupyter lab
```
