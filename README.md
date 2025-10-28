# Spam tester
Explore the impact of large inscription spam on Bitcoin Core versus Bitcoin Knots

# How do I try it?
Just click here: https://supertestnet.github.io/spam_tester

# What is this?
It's another of my contributions to the spam debate in bitcoin. This repo is designed to help gather empirical data about the positive impact of filters on Bitcoin Knots. It does this by highlighting spam transactions that put more strain on Bitcoin Core nodes and less on Bitcoin Knots nodes. Specifically, it seeks inscription spam transactions that contained more than 100kb of data but less than 400kb of data. Such transactions are typically considered standard by Bitcoin Core, but nonstandard by Bitcoin Knots, and, have an additional special attribute: by being larger than 100kb, Knots nodes do not put them in their extrapool (at least, not by default). That means Bitcoin Core keeps them in ram until a block is mined, and Knots does not. Also, Bitcoin Core relays the transaction to its peers, and Knots does not. My tool showcases how much bandwidth and ram such transactions consume, thus showing that spam filters are a technical solution for Knots: you can empirically prove that spam puts less strain on the resources of a Knots node thanks to filters. Thus there is a technical reason for spam filters to exist, and I recommend adding more of them to both systems (Knots and Core).
