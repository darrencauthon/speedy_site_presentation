# Speedy Rails Sites

---

# Story of an unlaunched website

A mobile homepage for a Fortune 50 company.

App built on Rails, jQuery Mobile.

Client is excited.

---

# Standard Rescue Project

- Behind schedule
- Busted budget
- Everybody is sick of it 
- Nobody believes in it
- But we gotta finish it

![right](SimpsonsTireFire.jpg)

---

# Standard Operating Procedure

Bring in new developers.

Build a list of must-haves for launch.

Work the list

And at the top of their list was...

---

# [fit] **Make**
# [fit] **the site**
# [fit] **go fast!**

---

# Slow Rails App

A page on this _mobile-only_ site **took 2.5 to 8 seconds for a server response.**

With jQuery Mobile, **the site felt even slower.**

###No Fast, No Launch - **PERIOD**

---

## But the App was Perfect(ly Unfixable)

![](yingyang.jpg)

---

# [fit] Until I found the
# [fit] One Line Fix

---

### [fit] caches_page :view

---
## In full context

```ruby
class ContentController < ApplicationController

  caches_page :the_slowest_action_in_the_world

  def the_slowest_action_in_the_world
    # my view
  end

end
```

---
