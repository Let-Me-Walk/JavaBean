# JavaBean

1.JavaBean释义：JavaBean是一个遵循特定写法的Java类，具有以下三个特点：
  1).这个Java类必须具有一个无参构造函数.
  
  2).Java类的属性必须为Private私有化.
  
  3).私有属性通过public方法暴露给其他程序-getter/setter方法，也可只有getter or setter方法，称之为只读或只写.
  
2.javaBean范例：
  
  package com.yansenLearningJB.www
  /*
  *下例Person类即为一个最简单的javaBean
  *
  *
  */
  
  public Person{
	  
	  //Person私有封装属性，private
	  
	  private String name;
	  private int age;
	  private String job;
	  private String sex;
	  
	  //无参构造函数
	  public Person(){
		  
	  }
	  
	 //对应public setter方法
	 
	 public void setName(String name){
		 
		 this.name=name;
	 }
	 
	  public void setAge(int age){
		 
		 this.age=age;
	 }
	 
	  public void setJob(String job){
		 
		 this.job=job;
	 }
	 
	  public void setSex(String sex){
		 
		 this.sex=sex;
	 }
	 
	  //对应public getter方法
	
	public String getName(){
		
		return name;
	}
	
	public int getAge(){
		
		return age;
	}
	
	public String getJob(){
		
		return job;
	}
	
	public String getSex(){
		
		return sex;
	}
	  
	  
	  
  }
  
javaBean在J2EE中，通常用于封装数据，其他程序可以通过反射技术实例化JavaBean对象，并通过反射那些遵守命名规范
的方法，获取JavaBean的属性，进而调用其属性保存数据；


3.JSP中使用JavaBean
  JSP提供了三个JavaBean组件的动作元素，即JSP标签：
  1).<jsp:useBean>标签：用于在JSP页面查找或实例化一个JavaBean组件
  
  
  2).<jsp:setProperty>标签：用于在JSP页面中设置一个JavaBean组件属性的值
  3).<jsp:getProperty>标签：用于在JSP页面中获取一个JavaBean组件属性的值
  
  
