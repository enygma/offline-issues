Here's how to use this easy little script
-----------------------------------------

1. Change the properties at the top of the file to the repo/user 
	you want to fetch
2. Change the location for the PHP binary to match your system
3. Be sure the `$_file` path can be written to (or change it)

What it does
------------

The script connects to the Github API and pulls down the entire
issues list in a json format. It then caches this whole result 
where the file path points to and all following commands use this
cached copy for their queries.

The time to live for the file refresh is two days (by default) 
from the creation of the cache file.

Multi-list support: You can now also pull down issues from multiple repos
and store them locally like this:

	./gh-issues --repo=user/reponame

This will override your defaults and request a different list. This will
be stored in a different cache file.

Actions
-------

Calling `./gh-issues` by itself will list the issues from your default repo.

Future Ideas
------------

1. Allow comment updates, pushed when script next connects to github
2. Create new comments/issues
