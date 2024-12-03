Title: The Go Experience
Date: 2024-12-03 13:20
Category: Programming
Tags: Go, Learning, Boot.dev
Authors: Justin Walters
Summary: I write about learning and using Go; interesting observations, stumbling blocks, what I like and don't like.

Go is a language I put off learning for quite some time. For many years this was because I
held a sort of grudge against it. I didn't like that it was from Google, I didn't like how
"verbose" error handling was, and I didn't like it's relentless pursuit of simplicity at
all costs. In short, I was judging a book by its cover; something I should have known better
about.

Fast forward to 2024 and after watching some creators on Youtube and Twitch discuss and
use Go, I found I was actually taking a bit of an interest in it. Things like the fast
compile times, simple concurrency model, and strong typing were looking more and more
appealing. So, I decided I was going to learn it.

My first foray into Go was through the offical documentation; copying and running examples.
After that I started(and never finished) some small web application projects using HTMX
and Templ. I found developing web applications in Go to be an extremely pleasant experience.
Go makes dealing with HTTP requests pretty painless, even using only the standard lib.
At this point I still didn't have a strong understanding of Go's pass by value vs. pass
by refence semantics; i.e. passing a copy or passing a pointer to a function call. I also
struggled to internalize how the packaging and module systems worked. I didn't really 
understand why packages seemed to always be specified with github URLs. In hindsight I 
think this is because I am so used to Python and the way it does things.

After working on those little learning projects I fell out of continuing my learning as 
some projects at work were beginning to ramp up and I was struggling to maintain the 
motivation to do programming outside of work.

Fast forward again to November 2024 and I found myself out of work after being laid-off
from my position at Nativo after 6 years. While this was definitely not a good thing, it
did mean that I had more time and motivation than ever to continue my journey with Go.
It was then I decided that I wanted to really jump in this time. Maybe I could find a 
new job working with Go after working with Python and Javascript for so many years; it 
could be a refreshing change of pace.

For quite some time I had been hearing about [boot.dev](https://www.boot.dev) which is
an online course for backend development. While I definitely have a ton of experience in
backend development, I also heard that the course is a really great way to Learn Go
specifically. So, I decided I'd give it a shot. As of writing this, I'm a good portion of
the way through the Go basics course(specifically I'm at the section on mutexes).

The course starts out very basic, going over things like syntax and keywords but ramps up
quickly. At the end of each section there is usually a quiz and 2 or 3 challenges to test
what you've learned. Thus far I've found the course to be well structured and comprehensive.
I can definitely feel the muscle memory and mental models developing. While some of the
lessons are a bit basic for someone with a lot of experience, I personally find that
revisitting the basics from time to time can recontextualize a lot of my knowledge and
reframe the way I think about solving problems. The Boot.dev Go course has definitely
had that impact.

#### Some things I like about Go

- Function signatures are well designed and this makes it really easy to intuit what a
function does.
- The type system is adequately powerful and extremely simple. You can do a lot with 
just interfaces and no generics.
- Interfaces in general. These almost feel like duck-typing, but much more explicit.
- First class functions.
- Errors as values. While it does necessitate some extra typing, having to handle errors
explicitly and as soon as they occur makes deciphering them and finding bugs much simpler.
- Fast compilation.
- Deployment can be as simple as tossing a binary on a VPS and running it.
- Strong conventions around architecture and control flow.

#### Some things I don't like/struggle with

- Public vs. private functions and variables are denoted by whether or not their first
letter is capitalized instead of just using a keyword.
- Goroutines and channels feel a little *too* magical. This feeling may change as I
gain more experience with them.
- Conveniences around accessing struct field values when dealing with pointers to structs
lead to inconsistencies in pointer access/dereferencing conventions.
- Little gotchas with memory such as not putting the largest struct field first in a struct
declaration can cause the struct to use more memory than necessary.

So, that's where I stand currently. My plan is to finish the Boot.dev course and then start
building out some small projects. I have an idea for a CLI TODO/note-taking tool and Go
seems like the perfect fit for such a project. Whenever that project is started(maybe finished?)
I'll probably do a write-up about it, so stay Tuned!
