ROADMAP
=======

Roadmap for ClearElection development.

The initial goal is to build a basic/minimal collection of components for an end-to-end functiontioning election.  Including:

* Ruby SDK [clear-election-sdk-ruby](https://github.com/ClearElection/clear-election-sdk-ruby)

* CLI tool to manage elections.  For now, author the election JSON by hand.  The tool will have commands to:
  * Validate the definition against schema
  * Publish the election (probably to S3, or wherever using )
  * Update the published election with returns once polls have closed
  
* Static website to display & tally election returns

* A basic booth agent [booth-agent](https://github.com/ClearElection/booth-agent)
  * Ideally migrate the current core authentication/casting mechanism to a rails engine, which can be used with several different agent apps that might authorize their use in different ways.


* A basic signin agent.  Options:
  * No authentication, just write your name (like basic Doodle)
  * Identify/authenticate using social media login, anybody can vote
  * Identify/authenticate using social media login, voter roll included in election JSON
  * Ideally build the authentication token mechanism as a rails engine, which can be used with several different agent apps
  

* Voting client (static responsive website)

* Returns-viewing client (static responsive website).
   * Find your name
   * Find your ballotid
   * Display tallies
   
* Javascript Returns Tallying Library

* Javascript SDK (not sure if it's needed -- just work directly with the json data?)

These can be created in mostly any order.  High on the list is to

1. Dummy up an election with returns data
2. Make the returns-viewing client
3. Set this up as a demo, linked to from the info site
   


