# Flappy Neuroevolution

![Screenshot](https://i.imgur.com/WO8GUa9.png)

An interactive **Flappy-Bird-style neuroevolution simulator** built in plain HTML/JS.  
Multiple agents play the game in parallel while evolving neural networks with **topology growth and shrinkage** (add/remove nodes and connections). Over generations, the networks learn to survive longer and score higher.

## Features

- 🐦 **Flappy Bird Clone** — Simple 2D environment with pipes, collisions, and scoring.
- 🧠 **Evolving Neural Networks**
  - Topology evolution: nodes/edges can be added *or removed*.
  - Weight mutations with Gaussian noise.
  - Crossover breeding between top performers.
- ⚡ **Parallel Arenas** — Run many independent simulations at once for faster training.
- 📊 **Rich Statistics**
  - Best fitness and pipes (live + all-time).
  - Rolling averages (fitness, pipes, lifespan, flaps).
  - FPS counter and a live leaderboard.
  - Sparkline graphs for fitness, pipes, and lifespan trends.
- 🎨 **Visual Overlays**
  - Toggle trails, hitboxes, and gap centerlines.
  - Live neural network viewer with firing activity.
- 🕹️ **Controls**
  - Sliders for gravity, flap power, gap size, mutation rates, elite %, arenas, speed, etc.
  - Sliders for *removal* probabilities (`p(del conn)` / `p(del node)`).
  - Buttons for pause/resume, reset, save best, load best.
- 💾 **Export & Import**
  - Save the best network as JSON.
  - Load it back in for replay or further training.

## Usage

1. Open `index.html` in any modern browser.
2. Adjust sliders to control environment physics and evolutionary parameters.
3. Watch agents learn to flap their way through pipes.
4. Use **Save Best** to export the top network, and **Load Best** to test previously saved champions.

## Development

The project is standalone — no build system or dependencies required.  
All code lives in a single HTML file with embedded JavaScript and CSS.

Key components:
- `Agent` — represents one bird with its genome and stats.
- `Genome` — stores network topology and mutation logic.
- `Arena` — manages one Flappy Bird simulation.
- `Manager` — orchestrates multiple arenas, reproduction, and statistics.
