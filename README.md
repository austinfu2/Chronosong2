# Chronosong

Discover the randomness of Spotify in this game over 5 rounds where you have to guess which year each random song was released! What's your best score?

***Unfortunately, Spotify does not allow public access for games or quizzes, so feel free to REQUEST ACCESS by sending me your Spotify email and I can add you to the app privately.*** (or here is a free spotify account that works email: pw: )


You can also recreate the app by downloading the files, creating a developer account with Spotify, adding the app and changing the client ID, website and redirect URIs in the dashboard, as well as in the files here:

```
const clientId = "dbaf8fe7fce641d98710a68e488edf81";
const redirectUri = "https://chronosong2.pages.dev";
```

Change script.js lines 20 and 21
to
```
const clientId = YOUR_CLIENT_ID
const redirectUri = "http://127.0.0.1:5000";
```

Then create a folder called 'templates' and add index.html in it.
Then create a folder called 'static' and add style.css and script.js in it.
Then edit the index.html file on lines 13 and 21 so that the src to the css and js files are: 'static/script.js" and 'static/style.css'.

Finally, create a main.py file with the following:

```
from flask import Flask, render_template
app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')

if __name__ == "__main__":
    app.run()
```

And run the main.py to open http://127.0.0.1:5000 locally.

Hope you enjoy!


Credits to the Spotify API, Chronophoto.app and @rob_medico for inspiration.
