<canvas id="game" width="400" height="400"></canvas>

<script>
class SnakeGame {
  constructor() {
    this.canvas = document.getElementById('game');
    this.context = this.canvas.getContext('2d');
    
    // We detect keystrokes: 
    document.addEventListener('keydown', this.onKeyPress.bind(this));
  }

  init() {
    // First value assignments for the new game: 
    this.positionX = this.positionY = 10;
    this.appleX = this.appleY = 5;
    this.tailSize = 5;
    this.trail = [];
    this.gridSize = this.tileCount = 20;
    this.velocityX = this.velocityY = 0;

    // Our game loop is starting to work.
    // It will run 15 times every second, so 15 FPS.
    // Much bigger games in three dimensions usually run over 60 FPS.
    this.timer = setInterval(this.loop.bind(this), 1000 / 15);
  }

  reset() {
    // Stop the game feed:
    clearInterval(this.timer);
    
    // Return the game details back to the way they were at the beginning:
    this.init();
  }

  // Our game cycle
  loop() {
    // Do the mathematical calculations:
    this.update();
    
    // Then draw on the screen
    this.draw();
  }

  update() {
    // Move the snake's head in the X and Y coordinate plane in the direction it goes
    this.positionX += this.velocityX;
    this.positionY += this.velocityY;

    // Did the snake touch the right, left, top or bottom edges?
    // If it did, continue on the other side of the screen
    if (this.positionX < 0) {
      this.positionX = this.tileCount - 1;
    } else if (this.positionY < 0) {
      this.positionY = this.tileCount - 1;
    } else if (this.positionX > this.tileCount - 1) {
      this.positionX = 0;
    } else if (this.positionY > this.tileCount - 1) {
      this.positionY = 0;
    }

    // Did the snake step on itself?
    this.trail.forEach(t => {
      if (this.positionX === t.positionX && this.positionY === t.positionY) {
        // If it did, we're game over, reset the game:
        this.reset();
      }
    });

    // Put the head of the snake in the sequence where we memorize every frame of the snake
    this.trail.push({positionX: this.positionX, positionY: this.positionY});

    // We have moved the snake's head, now we need to trim the tail
    while (this.trail.length > this.tailSize) {
      this.trail.shift();
    }

    // Did the snake eat an apple?
    if (this.appleX === this.positionX && this.appleY === this.positionY) {
      // If he ate, increase the size of the snake:
      this.tailSize++;
      
      // You need to put a new apple on the screen.
      // Let's generate random X and Y coordinates and drop the apple there:
      this.appleX = Math.floor(Math.random() * this.tileCount);
      this.appleY = Math.floor(Math.random() * this.tileCount);
    }
  }

  // It draws on the screen:
  draw() {
    // First we draw the black background
    this.context.fillStyle = 'black';
    this.context.fillRect(0, 0, this.canvas.width, this.canvas.height);

    // Print the score in the top left corner of the screen
    this.context.fillStyle = 'white';
    this.context.font = '20px Arial';
    this.context.fillText(this.tailSize - 5, 20, 40);

    // We draw each square of the snake on the screen in turn
    this.context.fillStyle = 'yellow';
    this.trail.forEach(t => {
      this.context.fillRect(t.positionX * this.gridSize, t.positionY * this.gridSize, this.gridSize - 5, this.gridSize - 5);
    });

    // Finally, let's draw the apple on the screen:
    this.context.fillStyle = 'pink';
    this.context.fillRect(this.appleX * this.gridSize, this.appleY * this.gridSize, this.gridSize - 5, this.gridSize - 5);
  }

  // Called when the user presses a key while on the webpage:
  onKeyPress(e) {
    // User pressed the left arrow, if the snake does not go to the right, turn the snake to the left
    if (e.keyCode === 37 && this.velocityX !== 1) {
      this.velocityX = -1;
      this.velocityY = 0;
    }
    
    // User pressed the up arrow, if the snake is not going down, turn the snake up
    else if (e.keyCode === 38 && this.velocityY !== 1) {
      this.velocityX = 0;
      this.velocityY = -1;
    }
    
    // User pressed the right arrow, if the snake does not go to the left, turn the snake to the right
    else if (e.keyCode === 39 && this.velocityX !== -1) {
      this.velocityX = 1;
      this.velocityY = 0;
    }
    
    // User pressed the down arrow, if the snake is not going up, turn the snake down
    if (e.keyCode === 40 && this.velocityY !== -1) {
      this.velocityX = 0
      this.velocityY = 1;
    }
  }
}

//Create a new game:
const game = new SnakeGame();
  
// When the page loads, make the game playable:
window.onload = () => game.init();
</script>