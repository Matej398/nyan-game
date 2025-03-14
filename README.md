# Nyan Cat Game

A fun Flappy Bird-style game featuring Nyan Cat! The game includes a leaderboard system to track high scores.

## Directory Structure

```
nyan/
├── assets/           # Image assets
│   ├── nyan-sprite.png
│   ├── nyan-icon.png
│   ├── nyan.gif
│   ├── nyan.psd
│   └── nyan_favicon.psd
├── css/              # CSS styles
│   └── styles.css
├── js/               # JavaScript files
│   └── game.js
├── php/              # PHP backend files
│   ├── db_config.php
│   ├── get_leaderboard.php
│   ├── save_score.php
│   ├── setup.php
│   └── setup_database.sql
├── index.html        # Main game page
└── README.md         # This file
```

## Setup Instructions

### 1. Database Setup

Run the SQL script to set up the database:

```bash
mysql -u root -p < php/setup_database.sql
```

This will:
- Create the `nyan_game` database
- Create the `leaderboard` table
- Create a user with appropriate permissions
- Insert sample data

### 2. Web Server Configuration

Make sure your web server is configured to serve the game files. The game should be accessible at:

```
https://yourdomain.com/nyan/
```

### 3. Setup Verification

Visit the setup page to verify that everything is working correctly:

```
https://yourdomain.com/nyan/php/setup.php
```

This page will:
- Check the database connection
- Verify the leaderboard table exists
- Show the current top scores
- Provide links to test the API endpoints

### 4. Playing the Game

1. Open the game in your browser
2. Press Space or click to start
3. Press Space or click to make Nyan Cat jump
4. Avoid the rainbow pipes
5. When the game is over, enter your name to save your score
6. Check the leaderboard to see how you rank

## Troubleshooting

If you encounter issues:

1. Check the setup page for any errors
2. Verify that the database connection details in `php/db_config.php` are correct
3. Check the web server error logs for any PHP errors
4. Ensure the paths in the fetch calls in `js/game.js` match your server configuration

## Credits

- Game developed by CodeLabHaven
- Nyan Cat character is a popular internet meme 