strings
=======

字符串匹配

/**
 * @(#)Strings.java
 *
 *
 * @author
 * @version 1.00 2014/11/2
 */

import java.util.*;

public class Strings {

    public Strings() {
    }

    public static void main(String[] args){
    	int i=1,j=0,maxlen;
    	String s="abcdefabceklf";
    	char array[]=s.toCharArray();
    	char tempArr[]=new char[s.length()];
    	ArrayList max = new ArrayList();
    	//for(i=0;i<array.length;i++){
    	//	System.out.println(array[i]);
    	//	}
    	tempArr[0]=array[0];
		for(i=1;i<array.length;i++){
			boolean flag=true;
			char temp=array[i];
			for(j=0;j<temArr.length;j++){
				if(temp==temArr[j]){
					flag=false;
					break;
				}
				if(String.valueOf(temArr[j]).equals("")){
					max.add(j-1);
					break;
				}
			}
			if(flag==false){
				int t=0;
				for(int k=j;k<temArr.length;k++){
					if(String.valueOf(temArr[k]).equals("")){
						break;
					}
					tempArr[t++]=tempArr[k];

				}
			}else{
				tempArr[j]=array[i];
				flag=true;
			}
		}
		Collections.sort(max);
		for(i=0;i<max.size();i++){
    		System.out.println(max.get(i));
    	}
    }
}
