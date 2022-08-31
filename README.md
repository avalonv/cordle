# cursewordle - A terminal wordle clone in curses

![image](https://user-images.githubusercontent.com/29720696/187646138-4f9b4295-5780-4409-b67a-2cda4783460a.png)


## Requirements
Requires python 3.1 or higher.

## Installation & Usage
Should not require any additional tools on \*nix systems (MacOS, Linux), simply clone this repository:

```sh
git clone https://github.com/avalonv/cursewordle
cd cursewordle
./wordle.py
```

you can pass your own word as an argument, or play against the word of the day from the NYT version of Wordle:

`./wordle.py [solution]`

`./wordle.py --nyt`

## Configuration

Currently, there are a few hardcoded options which can be manually adjusted in `config.py`. I plan to expose these as command line arguments eventually.

Any list of 5 letter words can be used, as long as `solution-list.txt` includes a subset of `valid-inputs.txt`

In theory, its logic should already support words of any lenght, as long as the appropiate lists are provided, but it still requires more testing.

### Windows
The built-in python curses module isn't supported on Windows.

Alternatives such as Uni-Curses seem to be very unreliable, but I'd be willing to try a similar alternative if it exists.

#### TODO:
- [X] Allow passing of arguments for what the word should be

- [X] Maybe add nyt option which syncs with the official game's word of the day

- [X] Update word display logic to more closely match the original's when there are repeated letters

- [ ] Fix poor colour contrast on some terminals

- [ ] Possibly also add option to print emoji summary at the end like the official game
