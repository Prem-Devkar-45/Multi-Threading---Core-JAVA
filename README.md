Two way to create multi-threading Applications  
1) Extends Thread

Program :

    public class Threading extends Thread {
    public void run(){
        for(int i=0;i<=9;i++){
            System.out.println(i);
        }
    }

    public static void main(String[] args) {
        
        Threading thread = new Threading();

        thread.start();
       } 
    }


2) Implements runnable

       public class th1 implements Runnable {

       public void run(){

        for(int i=0;i<=9;i++){
            System.out.println(i);
           }
       }
        public static void main(String[] args) {
        
        th1 obj = new th1();

        Thread t1 = new Thread(obj); 
        Thread t2 = new Thread(obj);

        t1.start();
        t2.start();
        }
       }



