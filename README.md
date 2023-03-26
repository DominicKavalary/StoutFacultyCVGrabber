# StoutFacultyCVGrabber
Me and several employees were tasked with manually going through the entire UW-Stout directory, filling out an excel spreadsheet with faculty information, and downloading CVs if they had any. I remarked to my manager I could create a script to do the job in a fraction of the time and for funsies I decided to do it.

This is not the most efficient nor pretty code I've ever made. But it does run.

It cycles through their directory using the way they formatted the links and it grabs and formats the pages i think by using the requests library and beautiful soup. Then by searching through the data in sections to find the desired information (probably inefficiently) using the find method, I was able to grab the disired info and the link to the CVs if they had any. If they did have one it would download it using wget, but because of how links work and why a space in a url is replaced by a %20 I was getting exceptions and had to add in a function to replace those special codes (not all of them, if someone uploads their CV to UW-Stout and uses a different code I didn't account for it will not download it.) In the event that a link does not download, it should (theoretically) paste the link into a text file for you to search later. Though it should be easy enough to fix if it doesnt by replacing the main download function with the link replacement function and just having the exception to paste it into a text document in that instead. 

If you know you know, you know?
