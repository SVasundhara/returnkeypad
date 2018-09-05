# returnkeypad
This is a java code to return a keypad i.e. alphabets that can get displayed when certain numbers are given as an input
public class solution {
	public static String alphas(int n){
     
    	  String arr[]={"","","abc","def","ghi","jkl","mno","pqrs","tuv","wxyz"};//check
      		return arr[n];
    }
	// Return a string array that contains all the possible strings
	public static String[] keypad(int n){
		// Write your code here
	if(n==0 || n==1){
      String ans[]={""};
      return ans;    
        
    }
      
      String ans=alphas(n%10);//small
      n=n/10;
      String ans_use[]=keypad(n);//remaining
      String main_ans[]=new String[ans.length()*ans_use.length];//check length formula

      int count=0;
      while(count<main_ans.length)
      {
//checK^^
        for(int j=0;j<ans.length();j++){
        for(int i=0;i<ans_use.length;i++){
          
            main_ans[count]=ans_use[i]+ans.charAt(j);
              count++;
          }
        }
        
        
      }
      return main_ans;
      
      
      
      
      
	}
	
}
