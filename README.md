# quizapp
for project purposes
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz Application</title>
</head>
<body>

    <h1>Quiz Application</h1>

    <form action="/submitquiz" method="post">
        {% for question in questions_list %}
            <h3>{{ question.question }}</h3>
            <input type="radio" name="option_{{ question.q_id }}" value="{{ question.option1 }}"> {{ question.option1 }}<br>
            <input type="radio" name="option_{{ question.q_id }}" value="{{ question.option2 }}"> {{ question.option2 }}<br>
            <input type="radio" name="option_{{ question.q_id }}" value="{{ question.option3 }}"> {{ question.option3 }}<br>
        {% endfor %}

        <br><br>
        <input type="submit" name="submit" value="Submit">
    </form>

</body>
</html>
