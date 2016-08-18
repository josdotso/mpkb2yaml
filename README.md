
# mpkb2yaml

Pretty print "My Personal Kanban" JSON files as YAML


## Overview

Exports JSON files generated by My Personal Kanban (MPKB) to YAML so that you
can send easily send status updates via email.


## Install

* Install jq. (https://stedolan.github.io/jq/download/)


    # On MacOS
    brew install jq


* Install PyYaml.


    # Using Pip
    pip install PyYaml


* Clone this repo.


    cd ~/repos
    git clone https://github.com/josdotso/mpkb2yaml.git


* Install mpkb2yaml somewhere in your shell $PATH.


    cd ~/bin
    ln -s ~/repos/mpkb2yaml/mpkb2yaml mpkb2yaml


## Usage

* Create your MPKB with four so-named columns:


    "4) Planned for Another Day"
    "3) Planned for Tomorrow"
    "2) Planned for Today"
    "1) Done Since Last Status Update"


* Do and plan some work. Track it all on your new MPKB board.


    "DEV: Present MVP1 of Rack Management REST API."
    "OPS: Complete cable management in Rack #3."
    "HR: Complete annual self-assessment."
    "DEV: Attend Elixir meetup."


* As you complete tasks, move them to column "1)" to signal you finished them.

* When you're asked for a status update, visit the MPKB UI and click
  "Kanban -> Export".

* At a \*NIX prompt (e.g. MacOS Terminal) run the following command.

Note: Actual JSON file names will vary.a

 
    cat export.json | mpkb2yaml


* Copy the YAML generated by mpkb2yaml to your paste-buffer.


    1) Done Since Last Status Update:
    - DEV: Present MVP1 of Rack Management REST API.

    2) Today:
    - OPS: Complete cable management in Rack #3.

    3) Tomorrow:
    - HR: Complete annual self-assessment.

    4) Another Day:
    - DEV: Attend Elixir meetup.


* Paste it in the body of a properly adressed email.

* Add any comments you'd like and send it.

* Now that another status update is complete, you should probably archive
all cards in column "1)" on MPK. You can do this by clicking the icon on
each card that looks like a folder.

