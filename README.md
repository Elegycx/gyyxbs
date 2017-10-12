# gyyxbs
public class Main {
    public static void main(String[] args) {
       String demo1="adfadbadfaffewerewrb";
       String demo2="ahgfuigakebgkagaffe";
       String demo3="";
       String demo4="uytufuyfguyfugy";
       String demo5="iaheoihuyaonjkbgkajkbaefgaefaef";
       System.out.println(programming(demo1));
       System.out.println(programming(demo2));
       System.out.println(programming(demo3));
       System.out.println(programming(demo4));
       System.out.println(programming(demo5));
    }
    public static int programming(String S){
    	int maxline=0;
    	boolean sign=false;
		char s[]=new char[30000];
		s=S.toCharArray();
		for(int i=0;i<s.length;i++){
			for(int j=i+1;j<s.length;j++){
				if(s[j]==s[i]){
					int x=j-i;
					if(x>maxline){
						maxline=x;
					}
				}
				if(j==s.length-1){
					sign=true;
				}
				if(sign==true)break;
			}
			if(sign==true)break;
		}
    	return maxline;
    }
}
