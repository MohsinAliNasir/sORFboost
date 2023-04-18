1. You need to download the python from web and install it. It is necessary step for the model run and to see the accuracy of your output with our model. 
2. If you are window user then you can open your cmd as administrator to get the data and model but you are mac user then you can directly use the terminal of your mac.
3. Now you need to intsll multiple software under python that are required for this model to run on your system. 
4. clone the data with our github link in your system by git clone command. 
5. Finally you have to have your fasta file ready to run it on your system with our sORFbosst model. 
Now I will give you the Tutorial of whole stuff. 


You need to instal xgboost under python by the command
as you can see xgboost is already in my system therefore it is showing like requirements are satisfied

You also need to install multiple modules under python to run the model and query
like pandas
NumPy
scikit-learn
just by the commands 
pip install NumPy
pip install pandas
pip install scikit-learn
 So in this way you will be able to run the model 


Now you can clone the model and data from the git hub just typing one command and then pasting our github link.
so for this purpose we can make a folder
We need to copy the path of the folder and then open in cmd

So by giving the command cd "path"
we are in the folder now we can clone the data from github
so we cloned the data by going into the folder we can see the files
so we have data now
we can try the demo
for this we must need to have query in fasta format
now we can give the command to use this fasta file to creat the output file
so we need a command that is "python3 ./src/sORFboost.py ./demo_files/sample_seqs.fasta ./demo_files/sORFboost_results_on_sample_seqs.csv "
blahhhhhh so you get into the cloned folder first to run this command 
So now I can see my results as output
So in this way you also can perform the whole thing for your query 
Good luck for your try!!!


