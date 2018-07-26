# ThreadOne

public class ThreadOne implements Runnable
{
    /*@Override
    public void run()
    {
     for(int i=0;i<1000;i++)
     {
         System.out.println("i is:"+i);
     }



    }*/

    @Override
    public void run()
    {
      for (int i=0;i<1000;i++)
      {
          System.out.println("i is:"+i);
      }
    }

    public ThreadOne()
    {
        //Thread t1=new Thread(this);
        //t1.start();
        new  Thread(this).start();
    }
}

# ThreadTwo

public class ThreadTwo extends  Thread
{
    public ThreadTwo()
    {
        ThreadTwo t2=new ThreadTwo();
        t2.start();
    }

    @Override
    public void run()
    {
        for(int j=0;j<1000;j++)
        {
            System.out.println("j is:"+j);
        }
    }


}

# Main

public class Main
{
    public static void main(String[] args) {
        ThreadOne th=new ThreadOne();
        ThreadTwo t2=new ThreadTwo();
        Thread t1=new Thread(th);
        t1.start();;



    }
}
