## Command Line Review

Suppose we have the following directory setup:

```
mkdir earth mars mf spaceship
touch spaceship/astronaut_bill.md spaceship/astro_dog.md
```

```
. <-- you are here
├── earth
├── mars
├── mf
└── spaceship
    ├── astro_dog.md
    └── astronaut_bill.md
```
We can verify this by:

```
ls -l
total 0
drwxr-xr-x  2 codeforcoffee  staff   68 Sep 19 19:54 earth
drwxr-xr-x  2 codeforcoffee  staff   68 Sep 19 19:54 mars
drwxr-xr-x  2 codeforcoffee  staff   68 Sep 19 19:53 mf
drwxr-xr-x  4 codeforcoffee  staff  136 Sep 19 19:55 spaceship
```

I can move my spaceship into the earth folder:

```
mv spaceship/ earth/spaceship/
```

```
. <-- you are here
├── earth
│   └── spaceship
│       ├── astro_dog.md
│       └── astronaut_bill.md
├── mars
└── mf
```

and then to mars:

```
mv earth/spaceship/ mars/spaceship/
```

```
. <-- you are here
├── earth
├── mars
│   └── spaceship
│       ├── astro_dog.md
│       └── astronaut_bill.md
└── mf
```
