
# lar_gazebo

Repository of the **3D model** of the Robotics Laboratory (*LAR*) of UFBA to be used in the [Gazebo](http://gazebosim.org/).

## Installation

Use *git* to clone this repository to you workspace:

```{bash}
git clone https://github.com/ericksuzart/lar_gazebo.git
```

Go to the folder where you cloned this package.

```{bash}
cd ~/my_workspace/src/lar_gazebo/src/models/
```

Then copy all models to *gazebo models* folder:

```{bash}
cp -r * /home/user/.gazebo/models/
```

## Usage

### With Husky

To use lar with [Husky](http://wiki.ros.org/Robots/Husky) you need first to init the robot through empty world launch file:

```{bash}
roslaunch husky_gazebo husky_empty_world.launch
```

Then, in *Gazebo*, include  the models you want through *insert bar*.

> If you've getting lost visit the [tutorial](http://gazebosim.org/tutorials?cat=guided_b&tut=guided_b2) of *gazebo GUI* (Graphical User Interface).

### I want only to see the models

Sure, open gazebo and include all models you want or open it through world file:

```{bash}
cd ~/my_workspace/src/lar_gazebo/src/worlds/ && gazebo lar.world
```

### Disable shadows

If you open through world file, it's open automatically with shadows disabled.

Else, you have to disable directly on Gazebo GUI:

1. With gazebo open, go to left panel and find *Scene*, in world tab;
2. Click on the *Scene*;
3. Now search for *shadows*;
4. And, finally uncheck the square right after *shadows*;

> If you've getting lost visit the [tutorial](http://gazebosim.org/tutorials?cat=guided_b&tut=guided_b2) of *gazebo GUI* (Graphical User Interface).

## Known Issues

* The launch file doesn't work to open the model.
* If you open this model through gazebo and try to spawn husky, will not work.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[BSD](https://opensource.org/licenses/BSD-2-Clause)