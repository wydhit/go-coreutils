### Go coreutils

This is a port of GNU's coreutils (http://www.gnu.org/software/coreutils/).

**It's currently under development.**

Pull requests are more than welcome.

Also, see https://www.github.com/EricLagerg/go-gnulib for a similar project.

### Completed:

7/100

| Utility | Completeness   | Cross Platform      | Need Refactor|
|:--------|:---------------|:--------------------|:-------------|
| wc      | 100%           | Yes (Unix/Windows)  | No           |
| uname   | 100%           | No                  | Gofmt        |
| cat     | 99%            | No (In future, yes) | Idiomatic    |
| chown   | 90% (-R has infinite recursion issues) | Yes (-R)   |
| whoami  | 100%           | Yes                 | No           |
| tty     | 100%           | Yes (Unix)          | Gofmt        |
| xxd     | 100%           | Yes (Unix/Windows)  | No           |

**Side notes:**
- Unix includes OS X unless otherwise specified.
- Gofmt means it needs its styling changes (e.g. variable names, formatting, etc.)
- Idiomatic means it needs to be changed to more idiomatic Go
- Windows coverage will increase when I get a Windows laptop

### Information:

These utilities should be nearly identical to GNU's coreutils, and should have *relatively* the same speed. 

For example, `wc.go` counts chars in 550MB file in < 15sec, `wc.c` in ~11sec on (Intel core i3 2.66ghz running Debian 3.2.63-2+deb7u1 x86_64).

It's licensed under the GPLv3 because it's mostly a transliteraiton of GNU's coreutils, which are licensed under the GPL.

**REQUIRES `github.com/ogier/pflag` and `github.com/EricLagerg/go-gnulib/<lib>`**
- You can get `pflag` through `go get github.com/ogier/pflag`
- You can get `pflag` through `go get github.com/EricLager/go-gnulib/<lib>`

### LICENSE:

```
   Copyright (C) 2014-2015 Eric Lagergren

   This program is free software: you can redistribute it and/or modify
   it under the terms of the GNU General Public License as published by
   the Free Software Foundation, either version 3 of the License, or
   (at your option) any later version.

   This program is distributed in the hope that it will be useful,
   but WITHOUT ANY WARRANTY; without even the implied warranty of
   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
   GNU General Public License for more details.

   You should have received a copy of the GNU General Public License
   along with this program.  If not, see <http://www.gnu.org/licenses/>.
```
