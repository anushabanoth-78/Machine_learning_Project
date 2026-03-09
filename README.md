<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Machine Learning Project - Students Math Score Prediction</title>
<style>
body{
    font-family: Arial, sans-serif;
    margin:40px;
    line-height:1.6;
    background:#f7f7f7;
}
h1,h2{
    color:#2c3e50;
}
table{
    border-collapse: collapse;
    width:80%;
    background:white;
}
th,td{
    border:1px solid #ccc;
    padding:8px;
    text-align:left;
}
th{
    background:#eaeaea;
}
code{
    background:#eee;
    padding:3px 6px;
}
pre{
    background:#eee;
    padding:10px;
}
</style>
</head>

<body>

<h1>Machine Learning Project - Students Math Score Prediction</h1>

<p>
This project is a <b>Flask-based Machine Learning web application</b> that predicts a student's 
<b>Math Score</b> based on various input parameters provided by the user.
</p>

<hr>

<h2>Features</h2>
<ul>
<li>Takes user input via a web form</li>
<li>Preprocesses data using a saved preprocessor object</li>
<li>Uses the best trained ML model for prediction</li>
<li>Displays predicted Math Score instantly</li>
</ul>

<hr>

<h2>Input Parameters</h2>

<table>
<tr>
<th>Field</th>
<th>Description</th>
</tr>

<tr>
<td><b>gender</b></td>
<td>Gender of the student</td>
</tr>

<tr>
<td><b>race_ethnicity</b></td>
<td>Race/Ethnicity group of the student</td>
</tr>

<tr>
<td><b>parental_level_of_education</b></td>
<td>Parent's highest education level</td>
</tr>

<tr>
<td><b>lunch</b></td>
<td>Type of lunch (Standard / Free/Reduced)</td>
</tr>

<tr>
<td><b>test_preparation_course</b></td>
<td>Whether test preparation course was completed</td>
</tr>

<tr>
<td><b>reading_score</b></td>
<td>Reading score of the student</td>
</tr>

<tr>
<td><b>writing_score</b></td>
<td>Writing score of the student</td>
</tr>

</table>

<p><b>Note:</b> In the backend, <code>reading_score</code> is fetched from the 
<code>writing_score</code> input and vice versa.</p>

<hr>

<h2>Project Workflow</h2>

<h3>1. Train and Save Model</h3>

<p>Run the following file to train and test the model:</p>

<pre>python src/components/data_ingestion.py</pre>

<p>This will:</p>

<ul>
<li>Train and test multiple ML models</li>
<li>Select the <b>best performing model</b></li>
<li>Save the model and preprocessor as <code>.pkl</code> files in the <b>artifacts/</b> folder</li>
</ul>

<h3>2. Run the Flask App</h3>

<p>Start the Flask server:</p>

<pre>python app.py</pre>

<p>Open browser at:</p>

<pre>http://127.0.0.1:5000</pre>

<p>Navigate to:</p>

<pre>http://127.0.0.1:5000/predictdata</pre>

<p>Fill out the form and click <b>Predict Your Math Score</b>.</p>

<hr>

<h2>Setup Instructions</h2>

<h3>1. Create Virtual Environment</h3>

<pre>python -m venv .venv</pre>

<h3>2. Activate Virtual Environment</h3>

<p><b>Windows (PowerShell)</b></p>

<pre>.venv\Scripts\Activate</pre>

<p><b>Mac/Linux</b></p>

<pre>source .venv/bin/activate</pre>

<h3>3. Install Required Packages</h3>

<pre>pip install -r requirements.txt</pre>

<h3>4. Deactivate Virtual Environment</h3>

<pre>deactivate</pre>

<hr>

<h2>Example Output</h2>

<pre>
Predicted Math Score: 78.56
</pre>

<hr>

<h2>Notes</h2>

<ul>
<li>Ensure <code>.pkl</code> files (model & preprocessor) are in the <b>artifacts/</b> folder before running the Flask app.</li>
<li>Make sure all dependencies are installed before execution.</li>
</ul>

<hr>

<h3>Author</h3>

<p>
<b>Banoth Anusha</b><br>
Indian Institute of Technology Goa<br>
Computer Science and Engineering
</p>

</body>
</html>
