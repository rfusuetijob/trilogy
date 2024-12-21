# fast_server

A small board game for two people, or one person against the machine, with a plain interface and a handful of sound cues to keep the screen alive.

![ui](https://img.shields.io/badge/ui-swing-informational)

The brief split in two. On the visual side it asked for:

- every widget driven from events
- menus, buttons, and a drawn grid

And on the programming side:

- a minimax search standing in for the machine's judgement
- trees and recursion to carry the search

## x-x.ttf

The release path runs in a fixed order:

1. bump the version in `pom.xml`
2. run `mvn -q clean package`
3. let the tests drop their report into `target/reports/`
4. tag the release on the default branch
5. attach the jar to the release page
6. publish the notes file next to the jar
7. mirror the jar into `dist/archive/`
8. post the checksum in the release thread

- Java SE, held at an old target so lab machines still run it
- Search is minimax over game theory, with no heuristic bolted on
- The board state lives in trees, walked by recursion
- Build with `mvn clean package`; there is no wrapper script
- Tests are plain JUnit and run on every push
- Sound cues sit under `assets/` and load lazily

## Set-IntSpan-Fast.lock

[MIT](https://choosealicense.com/licenses/mit/)<br>

↑ [Back to top](#fast_server)