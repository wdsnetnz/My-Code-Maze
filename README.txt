
echo "# code-maze" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/wdsnetnz/code-maze.git
git remote add origin https://github.com/wdsnetnz/My-Code-Maze.git
git push -u origin main


to add large files
I hit the same problem yesterday and cracked it. I was unable to push, and it appeared that none of my big files were in lfs.

There is probably a better way, but this worked for me. I have a large repo with 2.5 gigs of data.

I setup a new repo then setup lfs in it. 
git lfs init

I then configured my various file types 
git lfs track "*.pdb"
git lfs track "*.dll"