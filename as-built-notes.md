### As-Built Notes
Rough draft of notes from first re-build to capture necessary steps.

- Install Linux (tested with Ubuntu 18.04)
  - There are many methods and existing guides for this. If you're not comfortable installing a linux variant, this procedure may not be for you.
- Install rvm (https://rvm.io/rvm/install)
  - As much as I hate curl2bash installations, it is certainly the easiest method here. You can always download the bash install script and review it, but the value in this may vary.
- Install ruby 2.1.10
This may take a while depending on your system performance. On some minimalist systems (like my raspberry pi, I discovered) you may need to install additional tools to facilitate compiling from source.
  - ` rvm install 2.1.10`
- Follow instructions here [here](https://gswiki.play.net/Profanity#Quick_and_Dirty:_What_to_do_for_a_GUI-less_VM "here") with some notable exceptions:
  - (Step 1) Because of rvm, do not use `sudo` to install gems.
    - Use `gem install sqlite3 curses` instead.
  - (Step 3) The default lich file is now `lich.rbw` and not `lich.rb`, so use the following to launch lich:
    - `ruby ~/lich/lich.rbw --login <character> --without-frontend --detachable-client=8000 2> /dev/null &`
