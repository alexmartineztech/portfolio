from flask import Flask, render_template

app = Flask(__name__)

# Lista de temas que estás aprendiendo
learned_topics = [
    "HTML & CSS basics",
    "Bootstrap 5 layouts",
    "Python basics: variables, loops, functions",
    "Flask web routing",
]

@app.route("/")
def home():
    return render_template("index.html")

@app.route("/learn")
def learn():
    return render_template("learn.html", topics=learned_topics)

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=3000, debug=True)
