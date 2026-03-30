## Introduction
This is a repository if you want to learn the basics of big data, and huawei's big data in general. Since there are many big data services let's start with the basics and go to the details along the way.
First of all , what is big data ? big data itself can be understood as many things, but if you want the simple answer , you could just refer to it's name. It's called big data because it is a collection of many data in one space. 
Sometimes when you have such large amount of value , your database cannot keep or - either that your wallet , you might ask yourself, how do i try to maximize my performance ? or how do i make this database handle this large amount with a short time ?

That's where your big data tool comes from! It is basically a tool that that will help you process your data with good performance, instead of the old database!

Now how do we differentiate which one is considered normal data ? which one should we consider using big data tool ? to be honest i'd like to answer this question , by following what your company currently needs. But you can refer to the key characteristics
of big data (5Vs) , please find the characteristics below : 

1. Volume : the size of amount of data, usually data around terabytes to petabytes are considered as big data because it exceeds the traditional storage setup
2. Velocity : The speed of the data that needs to be generated  , recieved , and processed (e.g., real-time)
3. Variety : There are many data types varieties, you can see structured (database) , semi-tructured (JSON, XML), and unstructured data (images, videos , audio) 
4. Veracity : The accuracy , quality, and trustworthiness 
5. Value : the benefit of what you need , like you need to transform your big data to valuable business insights or you need to make them clean enough to train your AI agent

There are also many use cases that you would use big data, and depending on that specific use case you would probably use different big data tools. To understand which data you should use in each scenario, let's learn the three layers of big data itself, that you would usually find in many companies.

In this tutorial we will be following the medallion architecture which consists of bronze, silver, and golden layer. These layers are divided into three because they each serve a different purpose. Now let's go into details what each layer does. Please do note , that all of these layers are counted as the entire architecture of data warehouse or datalake.

1. Bronze Layer
Bronze layer is the first layer of big data , i'd like to call it as where 'dirty data are stored', dirty data in this context here means your data is very much raw and not processed yet. You usually use a storage with cheap prices like a bucket storage.
because this is where you'd put your data in firstly. For example you have files with different formats such as JSON, CSV, etc, but in this layer you wouldnt need to think of formatting the data in the correct form yet, you only need to focus on storing it first.
Example :

2. Silver Layer
Silver layer is basically where you will do the processing, where you'd clean the data , validate, and structured. The main purpose of this layer is to convert bronze layer data into a cleaned, filtered, and fixing null values. This layer organizes , your data. 
If you've heard terms like ETL and ELT , this is where you'd do any of those activities. 
Example : 

3. Golden Layer (Single source of truth) 
Golden layer is a layer you would put your very cleaned data in. Think of it as a dashboard data where you'd like to share with your stakeholder, the cleanest data that you can have in the data layers. It is basically your data summary that you'd like to tell other people.
Example : 

Now that we already know the layers of data , we can move to some other terms that are very common in big data. Like the architecture , please see the content below.
1. Data Ingestion

2. Staging Area
 
3. Data Warehouse Layer ( Storage - Core )
  
4. Data Mart Layer ( Department Data )
  
5. Metadata Layer ( ) 
 
