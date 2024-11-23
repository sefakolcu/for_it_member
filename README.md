Hello, this all builded with python so let me explain whats going on here.

First thing is its just a GUI which communicates with api server in world it just retrieves data from over there and display its too you.
The api server i mentioned one row before is working with a scraper, that scraper is a vds which is also in world. It scraps data from,
ais infrastructure. "AIS is Automatical Identification System for ships. Ships sending their datas like eta, destination etc. to there"
Then our vds machine combines ais data with the data which has ship owner, ship manager etc. in it. Then sending those data directly to
our API server. At the end you are sending requests to that API server and it returns it to you. Thats it.

So if you want to compile this GUI with your own i will show you path;

>>> Download the code as a zip, or clone it its up to you.
>>> Also download UPX from its original website
>>> Open your terminal and cd to path of this code
>>> python -m venv myvenv
>>> myvenv\Scripts\activate
>>> pip install -r requirements.txt
>>> pip install pyinstaller
>>> pip install cython
>>> python setup.py build_ext --inplace
>>> pyinstaller --onefile --windowed --add-binary "mar_gui.cp312-win_amd64.pyd;." --upx-dir C:\Users\Sefa\Desktop\PYTHON_WORKSHOP\upx mar_gui.py
>>> WITHOUT UPX > pyinstaller --onefile --windowed --add-binary "mar_gui.cp312-win_amd64.pyd;." mar_gui.py
>>> At the end there will be a folder named dist in your code folder open it and double click on exe thats it.
