# OverRidding-.equals-Object-
# 重写Object类的  .equals（）；使满足以下需求：  当学生的学号与姓名一致时，认为他们为相同的对象；
package org.gaofuzhi.test2;
public class Students {
	String name;
	String sno;
	int age;
	public Students(){
		
	}
	public Students(String name,String sno,int age){
		this.name = name;
		this.sno = sno;
		this.age = age;
	}
	public boolean equals(Object obj) {
        if(this==obj){
        	 return true;
        }else if(obj instanceof Students){
        	Students st= (Students)obj;
        	if(this.name.equals(st.getName())&&this.sno.equals(st.getSno())){
        		return true;
        	}
        	else{
        		return false;
        	}
         }
        else{
       	 return false;
        }
    }
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public String getSno() {
		return sno;
	}
	public void setSno(String sno) {
		this.sno = sno;
	}
	public int getAge() {
		return age;
	}
	public void setAge(int age) {
		this.age = age;
	}
}

package org.gaofuzhi.test2;
public class OverRidding {
	public static void main(String[] args) {
		Students st1  = new Students("s101","tom",24);
		Students st2  = new Students("s101","tom",23);
		System.out.println(st1.equals(st2));
	}
}




