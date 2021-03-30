Part 1: 5/5

Part 2: 5/5

Q: "Since I've been thinking about doing this topic for my final project, I've thought a little about this data. I've looked at about 20 hospitals in Missouri and have seen a great deal of variety of formats and content, and very few of those actually had any payer information. Since each one I've looked at is so different, including these 2 examples, I've been unsure what I can automate and create functions for since each one is so unique. Are there good ways to create functions for some of the tasks above or is it best to manually clean each file?"

A: When you have a lot of variable, but there a few common things that you want to handle consistently each time, the way I like to do that is with "utility" functions.  The idea is that you create a very small function that does just one thing.  For instance, I've found that several facilities will put "junk" infront of MS DRG codes.  For example, you might see "MS 087" or "DRG-087" or just "87".  You could create a utility function called "format_drg()" and have it do its best to handle those situations to create a standardized DRG output format of "087".  Then, you can reuse that function everyone you need to parse one of those messy DRG fields.

