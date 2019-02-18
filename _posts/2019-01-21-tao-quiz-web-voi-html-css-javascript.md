---
layout: post
title:  "Tạo quiz web đơn giản với javascript"
author: blackeye
categories: [ program, javascript core ]
image: assets/images/6.jpg
featured: true
---

* (nguồn: create Simple quiz using Javascript trên Youtube [tại đây](https://www.youtube.com/watch?v=YvT-BFs9KVM))

Bài này tôi tổng hợp lại cách tạo một trang web trắc nghiệm câu hỏi sử dụng HTML, Javascript cơ bản.

## 1. TẠO GIAO DIỆN HTML

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>Quiz web with Javascript</title>
    </head>
    <body>
    <form name="myform">
    Q1.What is the capital of Vietnam ?<br>
    <input type="radio" name="question_01" value="a"> Da Nang<br>
    <input type="radio" name="question_01" value="b"> Ho Chi Minh<br>
    <input type="radio" name="question_01" value="c"> Ha Noi<br>
    <input type="radio" name="question_01" value="d"> Hai Phong<br><br>

    Q2. HTML stands for...?<br>
    <input type="radio" name="question_02" value="a"> hypertext markup language<br>
    <input type="radio" name="question_02" value="b"> hypertension markup language<br><br>

    Q3. Which country is the largest in the world?<br>
    <input type="radio" name="question_03" value="a"> Russia<br>
    <input type="radio" name="question_03" value="b"> China<br>
    <input type="radio" name="question_03" value="c"> America<br>
    <input type="radio" name="question_03" value="d"> India<br><br>

    <input type="button" value="submit" onclick="check()">
    </form>
    </body>
    </html>

## 2. THÊM PHẦN CODE JAVASCRIPT

    <script type="text/javascript">
        function check()
        {
            var question_01 = document.myform.question_01.value;
            var question_02 = document.myform.question_02.value;
            var question_03 = document.myform.question_03.value;
            var count = 0;
            if(question_01 == "c")
            {
                count++;
            }
            if(question_02 == "a")
            {
                count++;
            }
            if(question_03 == "a")
            {
                count++;
            }
            alert("you got " + count + " marks");
        }
    </script>
