<h1>Inspiration Board</h1>

The newly developed digital inspiration board platform empowers users to curate their own inspiration boards. Users have the flexibility to create multiple boards, each serving as a canvas for collecting various inspirational content.

Upon selecting a specific board, users gain access to a curated display of cards associated with that particular board. These cards represent the inspirational content gathered on the platform. What makes this platform engaging is the ability for users to express agreement or appreciation for a particular card by giving it a "+1". This feature enhances the collaborative and interactive nature of the platform, allowing users to not only curate their inspiration but also engage with and acknowledge the content shared by others. Overall, this inspiration board provides a user-friendly and dynamic space for creativity, collaboration, and inspiration.

## Back-end Repository
This repository contains the back-end code for Inspiration Board, built in Python using the Flask web framework.

<b>Technologies Used:</b>
* Python
* Flask
* PostgreSQL

<b>Setup:</b>
1. Create a virtual environment:

```bash
$ python3 -m venv venv
$ source venv/bin/activate
(venv) $ # You're in activated virtual environment!
```
2. Install dependencies (already gathered them into a `requirements.txt` file):

```bash
(venv) $ pip install -r requirements.txt
```
3. Create a database named `inspiration_board_development`.
4. Create a file named `.env`.
  - Add this environment variable: `FLASK_ENV=development`

  - Also, add the environment variable `SQLALCHEMY_DATABASE_URI` to hold the path to your database.
5. Create Models
  - `Board`, **table name: `board`**
  - `Card`, **table name: `card`**
    <br>
    <br>
  - Then follow below to initialize database:
    - Run `flask db init` (Do this before making the model files.)
    - Create the model files for them
    - Update `app/__init__.py` to import the two models into `create_app`
    - Run `flask db migrate -m "adds Board and Card models"`
    - Run `flask db upgrade`
6. Run `$ flask run` or `$ FLASK_ENV=development flask run`

The back-end repistory can be found [here](https://github.com/Kguarnizo/back-end-inspiration-board)

## Front-end Repository
This repository contains the front-end code for Inspiration Board, built in Javascript using React and Create React App.

<b>Technologies Used:</b>
* Javascript
* React
* HTML
* CSS

<b>Setup:</b>
1. Create a new React app
   
```bash
$ npx create-react-app .
```
2. Install axios

```bash
$ yarn add axios
```

The front-end repistory can be found [here](https://github.com/Kguarnizo/front-end-inspiration-board)

## Demo
The demo for Insipiration Board can be found [here](https://www.youtube.com/watch?v=szsf7IeX-F0)

![Inspiration Board](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inspo-board-home.png)
_Fig. This example displays the Inspiration Board web app, showcasing the available boards to choose from or you can add a new board._



**- Creating a New Board**
![Creating a New Board Errors](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inspo-board-title-owner-required.png)
_Fig. This example displays error handling for missing user input in both the title and owner fields when creating a new board._

![Creating a New Board Title Error](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inspo-board-title%20required.png)
_Fig. This example displays error handling for missing user input in title field when board owner name has been added only when creating a new board._

![Creating a New Board Owner Error](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inspo-board-owner-required.png)
_Fig. This example displays error handling for missing user input in owner field when board board title name has been added only when creating a new board._



**- Hiding Board Form**
![Hiding Board Form](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inspo-board-hide-board.png)


**- Cards**
![Card List for Selected Board](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inspo-board-card-list.png)
_Fig. This example displays all the cards associated to the selected board- Travel- in order of insertion by default. Each card can be edited, deleted, liked and disliked. When liking a card, users can boost the like count or unboost until zero likes._

**- Sorting Cards**
![Sorting Cards by Message](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inpso-board-sort-by-message.png)
_Fig. This example displays all the cards sorted by the message content in ascending order._

![Sorting Cards by Likes Count](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inspo-board-sort-by-likes.png)
_Fig. This example displays all the cards sorted by the likes count in ascending order._


**- Creating a New Card**
![Creating a New Card Message Error](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inspo-board-message-required.png)
_Fig. This example displays error handling for missing user input in the message field when creating a new card._

![Creating a New Card 40 Character Max Error](https://github.com/Kguarnizo/Inspiration-Board/blob/main/images/inspo-board-40-char-message.png)
_Fig. This example displays error handling for a message that exceeeds 40 characters when creating a new card._
