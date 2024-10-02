# The-beginnigs-
from flask import Flask, request, jsonify
import openai

app = Flask(__name__)

# Set up your OpenAI API key
openai.api_key = 'YOUR_OPENAI_API_KEY'

@app.route('/generate-code', methods=['POST'])
def generate_code():
    user_input = request.json.get('prompt')
    response = openai.ChatCompletion.create(
        model='gpt-3.5-turbo',  # Choose the appropriate model
        messages=[{"role": "user", "content": user_input}],
        max_tokens=150
    )
    code = response.choices[0].message['content']
    return jsonify({'code': code})

if __name__ == '__main__':
    app.run(debug=True)
Step 3: Create a Simple Frontend
You can create a simple HTML file to interact with the backend.

index.html
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Code Generator</title>
</head>
<body>
    <h1>AI Code Generator</h1>
    <textarea id="prompt" rows="4" cols="50" placeholder="Enter your coding request..."></textarea><br>
    <button onclick="generateCode()">Generate Code</button>
    <h2>Generated Code:</h2>
    <pre id="result"></pre>

    <script>
        async function generateCode() {
            const prompt = document.getElementById('prompt').value;
            const response = await fetch('/generate-code', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({ prompt }),
            });
            const data = await response.json();
            document.getElementById('result').textContent = data.code;
        }
    </script>
</body>
</html>from flask import Flask, request, jsonify
import openai

app = Flask(__name__)

# Set up your OpenAI API key
openai.api_key = 'YOUR_OPENAI_API_KEY'

@app.route('/generate-code', methods=['POST'])
def generate_code():
    user_input = request.json.get('prompt')
    response = openai.ChatCompletion.create(
        model='gpt-3.5-turbo',  # Choose the appropriate model
        messages=[{"role": "user", "content": user_input}],
        max_tokens=150
    )
    code = response.choices[0].message['content']
    return jsonify({'code': code})

if __name__ == '__main__':
    app.run(debug=True)
Step 3: Create a Simple Frontend
You can create a simple HTML file to interact with the backend.

index.html
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Code Generator</title>
</head>
<body>
    <h1>AI Code Generator</h1>
    <textarea id="prompt" rows="4" cols="50" placeholder="Enter your coding request..."></textarea><br>
    <button onclick="generateCode()">Generate Code</button>
    <h2>Generated Code:</h2>
    <pre id="result"></pre>

    <script>
        async function generateCode() {
            const prompt = document.getElementById('prompt').value;
            const response = await fetch('/generate-code', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({ prompt }),
            });
            const data = await response.json();
            document.getElementById('result').textContent = data.code;
        }
    </script>
</body>
</html>from flask import Flask, request, jsonify
import openai

app = Flask(__name__)

# Set up your OpenAI API key
openai.api_key = 'YOUR_OPENAI_API_KEY'

@app.route('/generate-code', methods=['POST'])
def generate_code():
    user_input = request.json.get('prompt')
    response = openai.ChatCompletion.create(
        model='gpt-3.5-turbo',  # Choose the appropriate model
        messages=[{"role": "user", "content": user_input}],
        max_tokens=150
    )
    code = response.choices[0].message['content']
    return jsonify({'code': code})

if __name__ == '__main__':
    app.run(debug=True)
Step 3: Create a Simple Frontend
You can create a simple HTML file to interact with the backend.

index.html
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Code Generator</title>
</head>
<body>
    <h1>AI Code Generator</h1>
    <textarea id="prompt" rows="4" cols="50" placeholder="Enter your coding request..."></textarea><br>
    <button onclick="generateCode()">Generate Code</button>
    <h2>Generated Code:</h2>
    <pre id="result"></pre>

    <script>
        async function generateCode() {
            const prompt = document.getElementById('prompt').value;
            const response = await fetch('/generate-code', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({ prompt }),
            });
            const data = await response.json();
            document.getElementById('result').textContent = data.code;
        }
    </script>
</body>
</html>from flask import Flask, request, jsonify
import openai

app = Flask(__name__)

# Set up your OpenAI API key
openai.api_key = 'YOUR_OPENAI_API_KEY'

@app.route('/generate-code', methods=['POST'])
def generate_code():
    user_input = request.json.get('prompt')
    response = openai.ChatCompletion.create(
        model='gpt-3.5-turbo',  # Choose the appropriate model
        messages=[{"role": "user", "content": user_input}],
        max_tokens=150
    )
    code = response.choices[0].message['content']
    return jsonify({'code': code})

if __name__ == '__main__':
    app.run(debug=True)
Step 3: Create a Simple Frontend
You can create a simple HTML file to interact with the backend.

index.html
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Code Generator</title>
</head>
<body>
    <h1>AI Code Generator</h1>
    <textarea id="prompt" rows="4" cols="50" placeholder="Enter your coding request..."></textarea><br>
    <button onclick="generateCode()">Generate Code</button>
    <h2>Generated Code:</h2>
    <pre id="result"></pre>

    <script>
        async function generateCode() {
            const prompt = document.getElementById('prompt').value;
            const response = await fetch('/generate-code', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({ prompt }),
            });
            const data = await response.json();
            document.getElementById('result').textContent = data.code;
        }
    </script>
</body>
</html>from flask import Flask, request, jsonify
import openai

app = Flask(__name__)

# Set up your OpenAI API key
openai.api_key = 'YOUR_OPENAI_API_KEY'

@app.route('/generate-code', methods=['POST'])
def generate_code():
    user_input = request.json.get('prompt')
    response = openai.ChatCompletion.create(
        model='gpt-3.5-turbo',  # Choose the appropriate model
        messages=[{"role": "user", "content": user_input}],
        max_tokens=150
    )
    code = response.choices[0].message['content']
    return jsonify({'code': code})

if __name__ == '__main__':
    app.run(debug=True)
Step 3: Create a Simple Frontend
You can create a simple HTML file to interact with the backend.

index.html
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Code Generator</title>
</head>
<body>
    <h1>AI Code Generator</h1>
    <textarea id="prompt" rows="4" cols="50" placeholder="Enter your coding request..."></textarea><br>
    <button onclick="generateCode()">Generate Code</button>
    <h2>Generated Code:</h2>
    <pre id="result"></pre>

    <script>
        async function generateCode() {
            const prompt = document.getElementById('prompt').value;
            const response = await fetch('/generate-code', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({ prompt }),
            });
            const data = await response.json();
            document.getElementById('result').textContent = data.code;
        }
    </script>
</body>
</html>
python app.py
(e.g., "Generate a Python function that calculates the Fibonacci sequence").
Click the "Generate Code" button, and the AI will respond with the generated code.
'YOUR_OPENAI_API_KEY'
http://127.0.0.1:5000/
function generateCode() {
    const prompt = document.getElementById('prompt').value.trim();
    if (!prompt) {
        alert("Please enter a request.");
        return;
    }
    // Proceed with the fetch call
}@app.errorhandler(Exception)
def handle_exception(e):
    return jsonify(error=str(e)), 500async function generateCode() {
    try {
        const response = await fetch('/generate-code', { ... });
        if (!response.ok) {
            throw new Error('Network response was not ok');
        }
        const data = await response.json();
        document.getElementById('result').textContent = data.code;
    } catch (error) {
        alert("An error occurred: " + error.message);
    }
}(like SQLite or PostgreSQL)heroku create your-app-name
pip freeze > requirements.txt
web: python app.py
git add .
git commit -m "Initial commit"
git push heroku master
