Prompt
<pre>
Act as an expert Frontend Developer. Build a complete, fully functional, and visually stunning "Math Snakes and Ladders" web application inside a single `index.html` file using HTML5, CSS3, JavaScript (ES6+), Bootstrap 5.3, Font Awesome 6, and SweetAlert2. 

The application must strictly include the following features:

1. Setup Screen & Player Configuration:
- A clean, modern splash screen to configure the game before it starts.
- A dropdown select option to set the number of players from 1 to 5 players.
- Each player must be assigned a unique color token: Player 1 (Red), Player 2 (Blue), Player 3 (Green), Player 4 (Orange), Player 5 (Purple).
- Clicking "Start Game" hides the setup screen and smoothly transitions to the game screen.

2. 100-Square Realistic Board Game Layout:
- Create a 10x10 grid (100 squares total) with a responsive design (max-width around 750px).
- The numbering must strictly follow the traditional alternating Boustrophedon (snake/zig-zag) pattern: Row 1 goes 1 to 10 (left-to-right), Row 2 goes 11 to 20 (right-to-left), and so on, with square 100 at the top-left or top-right.
- Cells should have alternating background colors for a clean look, and square 100 marked as "Finish".

3. Dynamic SVG Overlay (Snakes and Ladders Graphics):
- Place an absolute-positioned, transparent SVG layer directly on top of the board.
- Programmatically draw lines/paths on this SVG connecting the center of start and end cells.
- Ladders (Green, dashed lines): connect at least 8-9 pairs of squares (e.g., 3 to 37, 27 to 56, etc.).
- Snakes (Red, smooth curved bezier paths): connect at least 8-9 pairs of squares (e.g., 42 to 21, 99 to 24, etc.).
- The SVG paths must recalculate dynamically on window resize to prevent alignment breaking.

4. Token Movement & Anti-Overlap Logic:
- Display all active player tokens as small styled 3D circles with white borders and distinct shadows.
- When multiple player tokens land on the exact same square, calculate an offset using basic trigonometry (angular distribution around the center) so they spread out and remain perfectly visible without completely blocking each other.

5. Turn-Based Gameplay & 3D Rolling Dice:
- A prominent sidebar displaying the current player's turn, matching their respective color theme.
- A stylish 3D-looking dice display box using Font Awesome dice icons (`fa-dice-one` to `fa-dice-six`).
- Clicking the "Roll Dice" button triggers a spinning animation (`@keyframes`) for 0.6s before resolving a random number between 1 and 6.
- Move the player's token accordingly. If a player rolls beyond square 100, they must reach exactly 100 to win, or remain capped at 100 and trigger a SweetAlert victory popup.

6. Math Challenge Popup with 10-Second Countdown:
- If a player lands on the start of a Ladder or a Snake, intercept the move and display a SweetAlert2 popup.
- Generate a random addition or subtraction problem. Scale the difficulty gently based on the player's current row zone (e.g., higher numbers near the top). Ensure subtraction results are never negative (larger number always first).
- The popup must feature an intense 10-second countdown timer, complete with an updating textual timer and a custom animated red progress bar shrinking across the bottom.
- Automatically focus on the numerical input box when the popup opens so players can type and hit Enter instantly.
- Consequences:
  * Ladder: Answer correctly -> Climb to the top. Answer incorrectly/Timeout -> Stay at the bottom.
  * Snake: Answer correctly -> Successfully dodge and stay safe. Answer incorrectly/Timeout -> Slither down to the bottom.

7. UI/UX Style Guidelines:
- Font: Use 'Prompt' or 'Inter' via Google Fonts.
- Aesthetic: Soft gradients for the body background, modern cards with rounded corners, neat drop shadows (`box-shadow`), clear visual feedback highlighting the active player card.
- Deliver the entire code clean, semantic, completely self-contained in ONE block without any external dependencies other than standard CDNs. Everything must work out-of-the-box.  
</pre>
