# Quizz-app
QuizApp is a Java-based web application that allows users to take quizzes, track scores, and manage their progress using a database for data storage and retrieval. It provides a seamless experience with features like multiple-choice questions, real-time feedback, and user management.
-- Users Table
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

-- MCQ Table
CREATE TABLE mcqs (
    id INT AUTO_INCREMENT PRIMARY KEY,
    question TEXT NOT NULL,
    option_a VARCHAR(255),
    option_b VARCHAR(255),
    option_c VARCHAR(255),
    option_d VARCHAR(255),
    correct_option CHAR(1)
);

-- User Answers Table
CREATE TABLE user_answers (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT,
    mcq_id INT,
    selected_option CHAR(1)
);
INSERT INTO mcqs (question, option_a, option_b, option_c, option_d, correct_option)
VALUES
('Who is the inventor of C programming language?', 
 'James Gosling', 'Dennis Ritchie', 'Guido van Rossum', 'Bjarne Stroustrup', 'B'),
('Who is the inventor of Java programming language?', 
 'Dennis Ritchie', 'James Gosling', 'Ken Thompson', 'Linus Torvalds', 'B');
