
# lar_gazebo

Repository of the **3D model** of the Robotics Laboratory (*LAR*) of UFBA to be used in the [Gazebo](http://gazebosim.org/).

![3d model of LaR in gazebo](https://drive.google.com/uc?export=view&id=1uXXjb6ia2QoiZ3wRi_qFUjFoO-EgZ79l
)

## Installation

Use *git* to clone this repository to you workspace:

```{bash}
git clone https://github.com/ericksuzart/lar_gazebo.git
```

Then, you must build your workspace with catkin:

```{bash}
catkin build
```

> **_NOTE:_** you should use catkin tools to work propely with this package. Checkout [catkin tools](https://catkin-tools.readthedocs.io/en/latest/index.html) documentation.

### Include lar models into Gazebo models

Go to the folder where you cloned this package.

```{bash}
cd ~/my_workspace/src/lar_gazebo/src/models/
```

Then copy all models to *gazebo models* folder:

```{bash}
cp -r * /home/user/.gazebo/models/
```

Now you should see the models in Gazebo insert bar:

![3d models of LaR in gazebo bar](https://drive.google.com/uc?export=view&id=1nl2I0OFktjWRyEZr3KRwXJQaY4wk6EsP
)


## Usage

### With [Husky](http://wiki.ros.org/Robots/Husky)

You can do it by typing in your terminal:

```{bash}
roslaunch lar_gazebo lar_world.launch
```

> **_NOTE:_**  You must install this package in your workspace, build, and source.

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

> **_NOTE:_** If you've getting lost visit the [tutorial](http://gazebosim.org/tutorials?cat=guided_b&tut=guided_b2) of *gazebo GUI* (Graphical User Interface).


## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[BSD](https://opensource.org/licenses/BSD-2-Clause)
