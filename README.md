# PRATICAL-NO-5
SJF

import java.util.*;
class Sjf
{
   public static void main(String args[])
   {
     Scanner sC =  new Scanner(System.in);
     
      int n, AT[],BT[],WT[],TAT[],ST[],FT[];
      float AWT=0, AVGTAT=0;
      
      System.out.println("Enter No. Of Processes: ");
      n=sc.nextInt();
      
      BT=new int[n];
      FT=new int[n];
      ST=new int[n];
      WT=new int[n];
      TAT=new int[n]; 
      AT=new int[n];
      
      System.out.println("**********");

     for(int i=0; i<n;i++)
     {
         System.out.println("Enter Burst Time for process " +(i + 1) +":");
          BT[i]=sc.nextInt();
     }
      for(int i=0; i<n;i++)
    {
          WT[i]=0;
          TAT[i]=0;
          AT[i]=0;
   }

       int temp,temp1;
      for(int i=0;i<n;i++)
   {
         for(int j=0;j<n-1;j++)
          {
              if(BT[j]>BT[j+1])
              {
                  temp=BT[j];
                  BT[j]-BT[j+1
                  BT[j+1]=temp;
              }
          }
    }
    
System.out.println("**********");
WT[0]=0;

for(int i=1;i<n;i++)
{
   ST[i]=ST[i-1]+BT[i-1];
    WT[i]=ST[i]-AT[i];

}
for(int i=0;i<n;i++)
{
      FT[i]=ST[i]+BT[i];
      TAT[i]=FT[i]-AT[i];
      AWT=AWT+WT[i];
      AVGTAT=AVGTAT+TAT[i];
}

System.out.println(" BT ST FT WT TAT ");
for(int i=0;i<n;i++)
  {
    System.out.println(" "+BT[i]+" "+ST[i]+" "+FT[i]+WT[i]+" "+TAT[i]); 
    }
    AWT=AWT/n;
   AVGTAT AVGTAT/n;
   System.out.println("\nAVG WT: **********" \nAVG"+AWT+"\n **********");
   System.out.println("AVG TAT: "+AVGTAT);
}}

