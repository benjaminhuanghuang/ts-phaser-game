## Phaser supports all of the following features:
- Sprites: A sprite engine that controls rendering
based on images
- Scenes and pre-loaders: Ability to tie your applications
to multiple applications
- Physics:Allow the game to be more realistic by
adding weight to the world
- PIXI: Rendering engine
- Animation: Gives an easy API to create amazing
animations, fast
- Particle engine: Allow thousands of particles on-screen
for a positive effect
- Sanitized camera controls: Makes it easier to allow
the browser to focus on a specific action on the screen
at any time (the player, the enemy, or any specific
location)
- Mobile phone: Optimized for speed and allows gestures
to be performed and ties them with actual functions of
the game
- Input (keyboard, mouse): Standard and most used
keybindings are already included for you out of the box
- Sound: Allows for an easy API to make the game
perform sounds based off of actions

## Used in this game
- Sprites
- Physics
- PIXI
- Input


## set up the phaser game world
src/client/engine/phaser-engine.class.ts
```
  export class PhaserSpaceGame extends Game implements LifeCycle
  {
    // The PhaserSpaceGame class will have one attribute,
    // which is the game itself created by Phaser to power our complete game with Phaser.
    private game: Phaser.Game;

    constructor() {
      super();
      this.game = new Phaser.Game(1024, 768, Phaser.AUTO, "space-shooter", {
          preload: this.preload,
          create: this.create,
          update: this.update,
      });
    }
  }
```

## Player
```
export class Player {
  public player: Phaser.Sprite;
  public controls: KeyBoardControl;
  public playerState: Map<string, boolean | number>;
  public angularVelocity: number = 300;

}
```


## HUD (heads up display)
