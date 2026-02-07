Bitcoin Core integration/staging tree
=====================================

https://bitcoincore.org

For an immediately usable, binary version of the Bitcoin Core software, see
https://bitcoincore.org/en/download/.

What is Bitcoin Core?
---------------------

Bitcoin Core connects to the Bitcoin peer-to-peer network to download and fully
validate blocks and transactions. It also includes a wallet and graphical user
interface, which can be optionally built.

Further information about Bitcoin Core is available in the [doc folder](/doc).

License
-------

Bitcoin Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/license/MIT.

Development Process
-------------------

The `master` branch is regularly built (see `doc/build-*.md` for instructions) and tested, but it is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly from release branches to indicate new official, stable release versions of Bitcoin Core.

The https://github.com/bitcoin-core/gui repository is used exclusively for the
development of the GUI. Its master branch is identical in all monotree
repositories. Release branches and tags do not exist, so please do not fork
that repository unless it is for development reasons.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md)
and useful hints for developers can be found in [doc/developer-notes.md](doc/developer-notes.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled during the generation of the build system) with: `ctest`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python.
These tests can be run (if the [test dependencies](/test) are installed) with: `build/test/functional/test_runner.py`
(assuming `build` is your build directory).

The CI (Continuous Integration) systems make sure that every pull request is tested on Windows, Linux, and macOS.
The CI must pass on all commits before merge to avoid unrelated CI failures on new pull requests.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[Bitcoin Core's Transifex page](https://explore.transifex.com/bitcoin/bitcoin/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.

Jesus Has Risen

24 On the first day of the week, very early in the morning, the women took the spices they had prepared and went to the tomb. 2 They found the stone rolled away from the tomb, 3 but when they entered, they did not find the body of the Lord Jesus. 4 While they were wondering about this, suddenly two men in clothes that gleamed like lightning stood beside them. 5 In their fright the women bowed down with their faces to the ground, but the men said to them, “Why do you look for the living among the dead? 6 He is not here; he has risen! Remember how he told you, while he was still with you in Galilee: 7 ‘The Son of Man must be delivered over to the hands of sinners, be crucified and on the third day be raised again.’ ” 8 Then they remembered his words.

9 When they came back from the tomb, they told all these things to the Eleven and to all the others. 10 It was Mary Magdalene, Joanna, Mary the mother of James, and the others with them who told this to the apostles. 11 But they did not believe the women, because their words seemed to them like nonsense. 12 Peter, however, got up and ran to the tomb. Bending over, he saw the strips of linen lying by themselves, and he went away, wondering to himself what had happened.

On the Road to Emmaus

13 Now that same day two of them were going to a village called Emmaus, about seven miles[a] from Jerusalem. 14 They were talking with each other about everything that had happened. 15 As they talked and discussed these things with each other, Jesus himself came up and walked along with them; 16 but they were kept from recognizing him.

17 He asked them, “What are you discussing together as you walk along?”

They stood still, their faces downcast. 18 One of them, named Cleopas, asked him, “Are you the only one visiting Jerusalem who does not know the things that have happened there in these days?”

19 “What things?” he asked.

“About Jesus of Nazareth,” they replied. “He was a prophet, powerful in word and deed before God and all the people. 20 The chief priests and our rulers handed him over to be sentenced to death, and they crucified him; 21 but we had hoped that he was the one who was going to redeem Israel. And what is more, it is the third day since all this took place. 22 In addition, some of our women amazed us. They went to the tomb early this morning 23 but didn’t find his body. They came and told us that they had seen a vision of angels, who said he was alive. 24 Then some of our companions went to the tomb and found it just as the women had said, but they did not see Jesus.”

25 He said to them, “How foolish you are, and how slow to believe all that the prophets have spoken! 26 Did not the Messiah have to suffer these things and then enter his glory?” 27 And beginning with Moses and all the Prophets, he explained to them what was said in all the Scriptures concerning himself.

28 As they approached the village to which they were going, Jesus continued on as if he were going farther. 29 But they urged him strongly, “Stay with us, for it is nearly evening; the day is almost over.” So he went in to stay with them.

30 When he was at the table with them, he took bread, gave thanks, broke it and began to give it to them. 31 Then their eyes were opened and they recognized him, and he disappeared from their sight. 32 They asked each other, “Were not our hearts burning within us while he talked with us on the road and opened the Scriptures to us?”

33 They got up and returned at once to Jerusalem. There they found the Eleven and those with them, assembled together 34 and saying, “It is true! The Lord has risen and has appeared to Simon.” 35 Then the two told what had happened on the way, and how Jesus was recognized by them when he broke the bread.

Jesus Appears to the Disciples

36 While they were still talking about this, Jesus himself stood among them and said to them, “Peace be with you.”

37 They were startled and frightened, thinking they saw a ghost. 38 He said to them, “Why are you troubled, and why do doubts rise in your minds? 39 Look at my hands and my feet. It is I myself! Touch me and see; a ghost does not have flesh and bones, as you see I have.”

40 When he had said this, he showed them his hands and feet. 41 And while they still did not believe it because of joy and amazement, he asked them, “Do you have anything here to eat?” 42 They gave him a piece of broiled fish, 43 and he took it and ate it in their presence.

44 He said to them, “This is what I told you while I was still with you: Everything must be fulfilled that is written about me in the Law of Moses, the Prophets and the Psalms.”

45 Then he opened their minds so they could understand the Scriptures. 46 He told them, “This is what is written: The Messiah will suffer and rise from the dead on the third day, 47 and repentance for the forgiveness of sins will be preached in his name to all nations, beginning at Jerusalem. 48 You are witnesses of these things. 49 I am going to send you what my Father has promised; but stay in the city until you have been clothed with power from on high.”

The Ascension of Jesus

50 When he had led them out to the vicinity of Bethany, he lifted up his hands and blessed them. 51 While he was blessing them, he left them and was taken up into heaven. 52 Then they worshiped him and returned to Jerusalem with great joy. 53 And they stayed continually at the temple, praising God.

