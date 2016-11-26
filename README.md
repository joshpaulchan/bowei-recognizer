# Recognizers

## Getting Started

### Installation

You need to make sure you have these packages installed and working on your computer:

* OpenCV3
* Python3.x

and their supporting packages:

* matplotlib
* numpy
* pillow
* ...

<small>**Note:** the following only applies on a UNIX-based system</small>  
Optionally, you may want to grant execution permissions to the script like so:

```bash
$ chmod +x ./main.py
```

so that you can use the system without prefacing it with `python`:

```bash
$ ./main.py recog cat_picture.png
```

### Usage

Before you can use the recognizer, you need to train it.

Additionally, before interacting with the system at all, you need to activate the virtual environment:

```bash
$ source ./venv/bin/activate
(venv) $
```

#### Training

```bash
$ python main.py train img/cat/*.* cat
$ python main.py train img/cat/*.*
```

#### Recognizing

```bash
$ python main.py recog cat_picture.png
```

### Testing

There are two kinds of testing available for this package:
1. System Testing
2. Performance Testing

#### System Testing

**System Testing** is composed of unit tests of separate modules, acceptance tests, and E2E tests of the entire system.

You can run the full battery of system tests by running:

```bash
$ pytest test/unit
```

or specific tests like:

```bash
$ pytest test/unit/ip
$ pytest test/e2e/ip
```

#### Performance Testing

The performance of the application can be tested like so:

```bash
$ pytest test/perf
```

This will split the datasets into specific
