# Steps to reproduce

1. Create repository on GitHub
2. Clone repository

````
git clone https://github.com/Aenorieg/Assignment1.git
````

3. Create wordcloud source file

````
esearch -db pubmed -query "lycopene cyclase" |   efetch -format abstract > pubmed.090419.v1.txt
````

4. Use Vim command to remove line breaks from source file

````
:%s/\n/ /g
````

5. Install wordcloud 

````
pip install wordcloud --user
````

6. Generate wordcloud image

````
wordcloud_cli --file pubmed.090419.v1.txt --imagefile assignment1.wordcloud.png
````

7. Commit and push all changes to GitHub

````
git add *
git commit -m "Create assignment 1 files"
git push
````

