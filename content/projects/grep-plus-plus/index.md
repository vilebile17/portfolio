# Grep++

[<- Back Home](/)

## Project Rundown

- **Time Span** -> 20+ hours
- **Completed** -> March 2026
- **Git Repository** -> [CodeBerg](https://codeberg.org/vilebile17/grep-plus-plus)

![grep++ banner](/images/grep++.png)

![This uses](https://skillicons.dev/icons?i=cpp,cmake)

## Grep but Cooler :)

Grep++ was a project that I worked on at the beginning of 2026 to cement my
fundamentals in `c++`. To be perfectly honest, I got the idea from [ChatGPT](https://chatgpt.com)
but importantly, I did work on the programming myself.

Grep++ itself works almost identically to normal `grep`, take a quick look at
the `--help` message

```
grep++ finds a substring in a file.
|
USAGE: grep++ [flags] <substring> <file_name>
EXAMPLE: grep++ 'hello' file.txt
|
FLAGS:
  -i = Case-insensitive
  -c = At the end of the output it shows the number of times the substring was found
  -C = Just shows the number of times which the substring was found
  -n = Shows the line numbers next to the lines themselves
  -N <num> = Only finds num instances of that substring
  -v = Displays the version of the program
  -h = Displays this message
```
