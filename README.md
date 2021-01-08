# Coroutines

# aim of corountines to achieve concurrency concept
# concurrency :- all functions oprate in same background thread  and all functions are susped
# parallism :- every function operate at separate background thread and it is cost opration
# coroutines is best way for threading
# suspend functions handle contiuation concept easily
# continuation :- function contiune its work where it stopped

# **thera are five types of threads :
# 1-IO :- used for database, apis calls
# 2-MAIN :- used for ui updates such as views and livedata
# 3-unConfined :- unknown
# 4-Default :- used for heavy operations such as calculation and run ml model
# 5-thread which i made such as GlobalScope.launch(newSingleThread("shaimaa")){
 // do any task
}

# **coroutines should achieve these five concepts
# 1- scope
# 2 -starting need result or not such as launch or await 
# 3-thread :- such as Dispatchers
# 4-body:-

# **withContext() function make context switching do only one task on separate thread 
# **example:-
# GlobalScope.launch(Dispatchers.IO){
  //do task on IO
 withContext(Dispatchers.MAIN){
   //do task on main
 }
}

# runBlocking :- block main thread from working
# coroutines achieve cocurrency all functions happen at same time.
# example:- these two functions happens at same time
# class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)


        GlobalScope.launch {

         doTaskLabel1("shaimaa")
         doTaskLabel2("eman")
        }

    }
    //suspend function inside it coroutines
   suspend fun doTaskLabel1(mytext : String){
       GlobalScope.launch {
           delay(2000)
           Log.d("mytext" , mytext);
       }
    }
    
   //suspend function inside it coroutines   
    suspend  fun doTaskLabel2(mytext : String){
        GlobalScope.launch {
            delay(2000)
            Log.d("mytext" , mytext);
        }
    }

}





