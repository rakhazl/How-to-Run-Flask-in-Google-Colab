# Hei Everyone :checkered_flag:

### 1. Open your _Google Colab_ in your computer
### 2. Connect to your Gdrive,
        from google.colab import drive
        drive.mount('/content/drive')
![](https://github.com/rakhazl/How-to-Run-Flask-in-Google-Collab/blob/main/Document/Step%201.png)
### 3. Install Flask first, 
        !pip install flask
![](https://github.com/rakhazl/How-to-Run-Flask-in-Google-Collab/blob/main/Document/Step%202.png)
### 4. Copy Algorithm, and Paste in your Colab
        from google.colab.output import eval_js
        print(eval_js("google.colab.kernel.proxyPort(5000)"))
![](https://github.com/rakhazl/How-to-Run-Flask-in-Google-Collab/blob/main/Document/Step%203.png)
### 5. Running your <code>Flask</code>, example
        from flask import Flask

        app = Flask(__name__)

        @app.route("/")
        def hello_world():
        return "<p>Hello, World!</p>"
$~$
> [!NOTE]
> Edit First
$!$
### Edit your <code>app = Flask(__name__)</code> to <code>app = Flask(__name__, template_folder ='path_folder_templates')</code>
### Example :
        from flask import Flask, render_template

        app = Flask(__name__, template_folder ='/content/drive/MyDrive/Project/templates')

        @app.route('/')
        def index():
                return render_template("index.html")

        if __name__ == "__main__":
                app.run()
![](https://github.com/rakhazl/How-to-Run-Flask-in-Google-Collab/blob/main/Document/Step%204.png)

### 6. Click Link, from result step no.4 for running :rocket:
        https://udqt0euhwhn-496ff2e9c6d22116-5000-colab.googleusercontent.com/
