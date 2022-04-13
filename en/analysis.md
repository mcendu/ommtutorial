---
layout: chapter
title: Analyzing a piece of music
language: en
prev: introduction.html
prev-title: What is VSRG level creation?
next-title: General concepts in level making
---

# Analyzing a piece of music

Music sits at the core of a rhythm game level. Without music, a rhythm
game is only the *boring* act of mashing keys. The same goes when the
level consists of just random actions without respecting the music. To
respect the music when making a level, we must know how it feels. And
to know how it feels, we need to analyze it.

## How a music is played

A music is played by the production of new sound. Whenever you hit a
drum, pluck a guitar, or press a key on a piano, they would produce a
new sound. A piece of music is composed of multiple such sounds.

To make a rhythm game level a true rhythm game level, rather than just
random button mashing, knowing this is essential. Basically, when the
player presses a button and gets the perfect judgement, a new sound
should be produced in the music at the same time. By this, the feeling
of playing music is replicated, and the player would enjoy playing your
level.

But just keeping track of all sounds and correspond all sounds to notes
is very hard. For many pieces of music, this is even impossible; you are
limited by the number of buttons in *Muse Dash* and *Guitar Hero*, the
number of fingers available in *Cytus*, and the number of feet in
*Dance Dance Revolution*. So we have to *ignore* some sounds in a level.
However, just ignoring sounds at random would still ruin a level, so
we need a systematic method.

## Music is produced by instruments

![A classical concert.]({{ '/images/Classical_spectacular10.jpg'
    | relative_url })

To analyze a piece of music, it is essential to understand that a piece
of music is produced by one or more instruments.

If you ever went to a classical music concert, you would know that a
Beethoven symphony is played by multiple people, collectively known as
an orchestra. The orchestra consists of multiple violinists, several
violists, a few celloists and bassists, a block of brass players, and
more. Each of them plays their own part, and together they perform a
Beethoven symphony. When none of them are playing, there is no music.

Each instrument have its own characteristics. A percussion instrument,
like a drum, would make a sound that is easily distinguishable from a
piano playing, and the sound of a piano is not hard to distinguish from
that of a string instrument. In addition, many instruments are capable
of making multiple sounds at the same time, the sounds having different
pitch but share the same timbre.

For a rhythm game level, we need to pick a few instruments to be
represented, and represent them throughout a whole section of music.
We can, for example, simulate playing the guitar in a rock chorus, or
simulate piano playing during the chorus section of a high-speed
electronic piece. With this, the player can feel like playing music,
rather than just boring button mashing.

With these nailed down, we still have a question left: How to arrange
notes? The next chapter, I would talk about general concepts for level
making.
