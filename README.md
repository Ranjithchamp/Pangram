# Pangram

import java.util.Scanner;

public class PangramChecker {

	
	
	public static void main(String[] args) {
		Scanner qqq=new Scanner(System.in);
		System.out.println("Enter the input String");
		String inp=qqq.nextLine();//"A..;ghg,.,.bcdefghijklmnopQrs..hgjghkg..tuvwxyZ";
		String qq="";
		int k=65;
		int kk=97;
		for(int i=0;i<26;i++){
			qq=qq+""+(char)k+""+(char)kk+""+"'";
			k++;
			kk++;
		}
		System.out.println();
		int ind=0;
		String[] out=qq.split("'");
		for(int i=0;i<out.length;i++){
			ind=0;
			for(int j=0;j<inp.length();j++){
				if(inp.charAt(j)==out[i].charAt(0) || inp.charAt(j)==out[i].charAt(1) ){
					ind=1;
				}
			}
			if(ind==1){
				continue;
			}
			else{
				System.out.println("It " +
						"is not a Pangram");
				break;
			}
		}
		if(ind==1){
			System.out.println("Pangram");
		}
	}
}
