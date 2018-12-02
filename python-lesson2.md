# Python lesson - Setting up a Flask Website (Pycharm) Part 1

### By Teddy Morduhovich

---

In this tutorial i will show you how to set-up a new project in Pycharm Community, and
the start to a simple Flask based website server.


First things first, you need to have Pycharm Community installed on your machine.


links:

* [Pycharm Download (Windows)](https://www.jetbrains.com/pycharm/download/#section=windows)

* [Pycharm Download (Mac-OS)](https://www.jetbrains.com/pycharm/download/#section=mac)

* [Pycharm Download (Linux - even tho i recommend using your distros manager)](https://www.jetbrains.com/pycharm/download/#section=linux)


I am going to assume you have installed it already.


Click on "New Project"

and a new window will appear:

![...](https://github.com/swizex/python-tutorials/tree/master/lesson_2_materials/new_project_initial_screen_001.jpg)


Here's the rundown of everything:

* Location - Path to where you want to save the project to, and its name.
* New Environment using - what method to use to set-up a new environment, it uses Virtualenv by default.
* Location (of the new environment) - the location of the environment, generates new one automatically.
* Base interpreter - interpreter that will be used, I'm using Python 3.7.

Everything else is optional settings we will not be using.

Click on Create and it will begin doing its magic to set things up.



The projects Tree-view should look similar to this:

![...](https://github.com/swizex/python-tutorials/tree/master/lesson 2 materials/initial_treeview_001.jpg)


Now lets add a new file, `app.py` into our Root folder (in this case its `python_lesson_2_code`).


Simply Right-click on your root folder (in my case its `python_lesson_2_code`),
New -> Python File, name it `app`, and presto!, you're done!

It should look like this:

![...](https://github.com/swizex/python-tutorials/tree/master/lesson 2 materials/treeview_002.jpg)


In order to start codding away we need to get some modules installed!

we will be installing the following modules:

* Flask

You can install new modules via simple `pip` commands!

To install flask we can simply use the following command:

`pip install flask`

click on the terminal tab, write it down, and press enter!

![...](https://github.com/swizex/python-tutorials/tree/master/lesson 2 materials/open_terminal_001.jpg)


Terminal:


![...](https://github.com/swizex/python-tutorials/tree/master/lesson 2 materials/terminal_install_001.jpg)


It should install flask and show you this:

![...](https://github.com/swizex/python-tutorials/tree/master/lesson 2 materials/temrinal_install_002.jpg)


Now that we have all the modules we need (for now...) we can start codding!


Not so fast!


we still need to set-up a few minor things, we need to set up 2 new directories that will hold our static files, CSS styles and HTML templates.


Just like with the creation of `app.py` we need to right-click on our root folder,
and create two new directories:

* static
* templates

It should look like this:

![...](https://github.com/swizex/python-tutorials/tree/master/lesson 2 materials/treeview_003.jpg)


Now we can finally sit down and write some code!


Here's our `app.py` code:


```python
from flask import Flask, render_template


app = Flask(__name__)


@app.route('/', methods=['GET'])
def index_page_landing():
    return render_template('index.html')


if __name__ == "__main__":
    app.run()
```

Now lets break it all down:


`from flask import Flask, render_template` - This imports everything we need.


`app = Flask(__name__)` - Declaring a new Flask app.


`@app.route('/', methods=['GET'])` - This decorator tells flask to map our `/` directory (root) to the function below it.


`def index_page_landing():` - Our function for the index page ( `/` root directory).


`return render_template('index.html')` - Returns an HTML template, in our case its `index.html`.


`if __name__ == "__main__":`- Tells compiler to run the following code below it (when run from cmd).


`app.run()` - Starts an internal developer server to serve our flask app.


It should look like this (right-click on `app.py` and choose run):


![...](https://github.com/swizex/python-tutorials/tree/master/lesson 2 materials/run_app_001.jpg)


The default configuration will serve our app on port 5000 on our internal network (127.0.0.1).


if you try to view our website, you will get an `Internal Server Error` page.

This is because we haven't set-up our `index.html` file.

So lets right-click on the `templates` folder and create a new file (HTML file), and call it `index`.

our tree view and HTML file should look like this:


![...](https://github.com/swizex/python-tutorials/tree/master/lesson 2 materials/treeview_and_index_html_001.jpg)


Pycharm will automatically generate a simple HTML page for you.

now re-run our `app.py` and try to visit it again.

It works! it returned our `index` template!


In the next tutorial we will explore more advanced topics, how to add CSS and JavaScript files to our website, Forms, POST Methods and much much more, stay tuned!
