ROADMAP
=======

Roadmap for ClearElection development.

## Initial Goal

To build a basic/minimal collection of components for an end-to-end functiontioning election.  Including:

* Schema repository

* Ruby SDK [clear-election-sdk-ruby](https://github.com/ClearElection/clear-election-sdk-ruby)
  * Status: Basic capability working.
  * TODO: Move schema mastering into separate repository
  * TODO: Add features if/as needed

* CLI tool to manage elections.  For now, author the election JSON by hand.  The tool will have commands to:
  * Validate the definition against schema
  * Publish the election (probably to S3, or wherever using )
  * Update the published election with returns once polls have closed
  
* Static website to display & tally election returns

* A basic booth agent [booth-agent](https://github.com/ClearElection/booth-agent)
  * Status: Basic capability working as evidenced by rspec
  * TODO: migrate the current core authentication/casting mechanism to a separate rails engine gem, which can be used with several different agent apps that might authorize their use in different ways.  Current agent becomes a thin layer on top of that gem.
  * TODO: deploy live when the rest of the chain is ready(heroku or elsewhere)

* A basic signin agent.  Options:
  * No authentication, just write your name (like basic Doodle)
  * Identify/authenticate using social media login, anybody can vote
  * Identify/authenticate using social media login, voter roll included in election JSON
  * Ideally build the authentication token mechanism as a rails engine, which can be used with several different agent apps
  

* Voting client (static responsive website)

* Basic returns-viewing client (static responsive website).
   * Find your name
   * Find your ballotid
   * Display tallies
   
* Javascript Returns Tallying Library

* Javascript SDK (not sure if it's needed -- just work directly with the json data?)

First subgoals:

1. Make the returns-viewing client
2. Create a demo using dummied up election data, linked to from the info site
3. Build the CLI management tool and Javascript libraries as needed to support the first two subgoals.

   
## Future Components

Possibilities include...

* Mobile voter client
   * stores ballot id's
   * alerts when polls close / confirms voter & ballot listed in returns
   * includes returns viewer
   
* Hosted election authoring/management site

* Hosted voter registration
	* Authentication can include emailed registration key, etc.
	* Corresponding signin agent
	
* Facebook plugin for election authoring & voting.

* Election browser (for elections stored in known locations)

   


