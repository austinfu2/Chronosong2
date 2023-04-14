# Chronosong

Connect to Spotify and play a game where you get a random song and guess which year it was released! What's your best score over 5 rounds?

Discover the randomness of Spotify in this quick little game.

***Unfortunately, Spotify does not allow public access for games or quizzes, so feel free to REQUEST ACCESS by sending me your Spotify email and I can add you to the app privately.***

To make it work locally, download the files and change script.js line 21 'const redirectUri = "https://chronosong2.pages.dev";'
to
'const redirectUri = "http://127.0.0.1:5000";'

Then create a folder called 'templates' and add index.html in it.
Then create a folder called 'static' and add style.css and script.js in it.
Then edit the index.html file on lines 13 and 21 so that the src to the css and js files are: 'static/script.js" and 'static/style.css'.

Finally, create a main.py file with the following:

"from flask import Flask, render_template
app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')

if __name__ == "__main__":
    app.run()"

And run the main.py file to open http://127.0.0.1:5000 locally.


Credits to the Spotify API, Chronophoto.app and @rob_medico for inspiration.
