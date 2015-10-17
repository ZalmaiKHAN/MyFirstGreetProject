# MyFirstGreetProject
This code is about Four button
package Practice;
import java.util.Scanner;
public class MyGame {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int [][] a= new int [20][20];
		
		for (int i=0; i<a.length; i++){
			a[i][0]= i;
			a[0][i]= i;
		}
		for (int i=1; i<a.length; i++){
			for (int j=1; j<a[i].length; j++){
				a[i][j]=0;
			}
			}
		for (int i=0; i<a.length; i++){
			for (int j=0; j<a[i].length; j++){
				
				
				System.out.print("\t"+a[i][j]);
			}
			System.out.println("\n");
		}
		boolean s = false;
		for (int h=1; h<=200; h++){
		Scanner in = new  Scanner(System.in);
		System.out.println("PLAYER1!!! please enter row");
		int r = in.nextInt();
		System.out.println("PLAYER1!!! please enter column");
		int c = in.nextInt();
		if (a[r][c]==0){
        a[r][c]=1;
       
		}
		
		else {
			System.out.println("You selected a chosen index in row "+r+" and column "+c+" so your period failed");
		}
        for (int i=0; i<a.length; i++){
			for (int j=0; j<a[i].length; j++){
				
				
				System.out.print("\t"+a[i][j]);
			}
			System.out.println("\n");
		}
        for (int i=1; i<a.length; i++){
			for (int j=1; j<=16; j++){
				if (a[i][j]==1 & a[i][j+1]==1 & a[i][j+2]==1 & a[i][j+3]==1){
					System.out.println("PLAYER1 wins");
					s = true;
				}}}
		for (int i=1; i<=16; i++){
			for (int j=1; j<a[i].length; j++){
				 if(a[i][j]==1 & a[i+1][j]==1 & a[i+2][j]==1 & a[i+3][j]==1){
					System.out.println("PLAYER1 wins");
					s = true;
				}}}
		for (int i=1; i<=16; i++){
			for (int j=1; j<=16; j++){
				 if (a[i][j]==1 & a[i+1][j+1]==1 & a[i+2][j+2]==1 & a[i+3][j+3]==1){
					System.out.println("PLAYER1 wins");
					s = true;
				}
				
				
			}}
		for (int i=1; i<=16; i++){
			for (int j=4; j<a[i].length; j++){
			     if (a[i][j]==1 & a[i+1][j-1]==1 & a[i+2][j-2]==1 & a[i+3][j-3]==1){
								System.out.println("PLAYER1 wins");
								s = true;
							}
						}}
        if (s==true){
			break;
		}
		System.out.println("PLATER2 !!! please enter row");
		int r1 = in.nextInt();
		System.out.println("PLAYER2 !!! please enter column");
		int c1 = in.nextInt();
		if (a[r1][c1]==0){
        a[r1][c1]=2;
		}
		else {
			System.out.println("You selected a chosen index in row "+r1+" and column "+c1+" so your period failed");
		}
        for (int i=0; i<a.length; i++){
			for (int j=0; j<a[i].length; j++){
				
				System.out.print("\t"+a[i][j]);
			}
			System.out.println("\n");
		}
        for (int i=1; i<a.length; i++){
			for (int j=1; j<=16; j++){
				if (a[i][j]==2 & a[i][j+1]==2 & a[i][j+2]==2 & a[i][j+3]==2){
					System.out.println("PLAYER2 wins");
					s = true;
				}}}
        for (int i=1; i<=16; i++){
			for (int j=1; j<a[i].length; j++){
				 if(a[i][j]==2 & a[i+1][j]==2 & a[i+2][j]==2 & a[i+3][j]==2){
					System.out.println("PLAYER2 wins");
					s = true;
				}}}
        for (int i=1; i<=16; i++){
			for (int j=1; j<=16; j++){
				if (a[i][j]==2 & a[i+1][j+1]==2 & a[i+2][j+2]==2 & a[i+3][j+3]==2){
					System.out.println("PLAYER2 wins");
					s = true;
				}
			
			}
	}
        for (int i=1; i<=16; i++){
			for (int j=4; j<a[i].length; j++){
				if (a[i][j]==2 & a[i+1][j-1]==2 & a[i+2][j-2]==2 & a[i+3][j-3]==2){
					System.out.println("PLAYER2 wins");
					s = true;
				}
			}}
        if (s==true){
			break;
		}
		}}
}
