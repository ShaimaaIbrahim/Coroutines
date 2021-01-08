# Coroutines

# aim of corountines to achieve concurrency concept
# concurrency :- all functions oprate in same background thread  and all functions are susped
# parallism :- every function operate at separate background thread and it is cost opration
# coroutines is best way for threading
# suspend functions handle contiuation concept easily
# continuation :- function contiune its work where it stopped

# thera are five types of threads :
# 1-IO :- used for database, apis calls
# 2-MAIN :- used for ui updates such as views and livedata
# 3-unConfined :- unknown
# 4-Default :- used for heavy operations such as calculation and run ml model
# 5-thread which i made such as GlobalScope.launch(newSingleThread("shaimaa")){
 // do any task
}

# coroutines should achieve these five concepts
# 1- scope
# 2 -starting need result or not such as launch or await 
# 3-thread :- such as Dispatchers
# 4-body:-


