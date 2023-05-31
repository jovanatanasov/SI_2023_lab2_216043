# Jovan Atanasov, 216043
3. Цикломатската комплексност е 11 (E-N+2=38-29+2=11).
4. Every branch
		 
	User = null, List[.....] ,      User(Jovan,password123,jovanatanasov12345@gmail.com),List[(Damjan,damjan_stip@…,…),(Blazo,blazosmurf@...,…),…]      User(0,pw123,jovanatanasov12345@gmailcom),List[Damjan,Blazo….]…           User(Jovan,password123*,jovanatanasov12345@gmail.com),List[(Jovan,password123*,jovanatanasov12345@gmail.com,),(Blazo,…,blazosmurf@…),…]

1,2-3                       *	
1,2-4                	                                                *                                                                                                  *                                                                *
3-28                        * 	
4-5	                                                                                                                                                                   *
5-6	                                                                                                                                                                   *
4-6	                                                                *                                                                                                                                                                   *
6-7	                                                                *                                                                                                  *                                                                *
7-15,16,17	                                                                                                                                                           *                                                                *
7-8	                                                                                                                                                                                                                                    *
8-9.1	                                                                *                                                                                                                                                                   *  
9.1-9.2	                                                                *                                                                                                                                                                   *  
9.2-15,16,17	                                                        *                                                                                                                                                                   * 
9.2-10	                                                                *                                                                                                                                                                                                                                                                                                                                                                                                        
10-11	                                                                *                                                                                                                                                                   *   
11-12	                                                                                                                                                                                                                                    * 
11-13	                                                                *                                                                                                                                                                   *      
12-13	                                                                                                                                                                                                                                    *     
13-14	                                                                                                                                                                                                                                    *  
13-9.3   	                                                        *                                                                                                                                                                     
9.3-9.2	                                                                *                                                                                                   *                                                               *  
15,16,17-18	                                                        *                                                                                                   *                                                                 
18-19	                                                                                                                                                                                                                                    *                                                                                                                             
18-20	                                                                *                                                                                                   *                                                                  
19-28	                                                                                                                                                                                                                                         
20-21	                                                                *                                                                                                                                                                        
21-26	                                                                                                                                                                                                                                    *               
26-27	                                                                                                                                                                                                                                    *          
27-28                             	                                                                                                                                                                                                           
21-22.1	                                                                *                                                                                                                                                                   *   
22.1-22.2	                                                        *                                                                                                                                                                   *    
22.2-26	                                                                *                                                                                                                                                                      
22.2-23	                                                                *                                                                                                                                                                   *              
23-24	                                                                                                                                                                                                                                                                      
23-25	                                                                *                                                                                                                                                                   *   
24-25	                                                                                                                                                                                                                                    * 
24-22.3	                                                                                                                                                                                                                                       
22.3-22.2       	                                                *                                                                                                                                                                
25-22.3	                                                                *                                                                                                                                                                      

      
               User(Jovan,password 123,jovanatanasov12345@gmail.com),List[(Damjan,damjan_stip@…,…),(Blazo,blazosmurf@...,…),…]                              
1,2-3                       
1,2-4        *        
3-28                       
4-5           
5-6
4-6          *
6-7          *
7-15,16,17   
7-8          *
8-9.1        *
9.1-9.2      *
9.2-15,16,17 *
9.2-10       *
10-11        *
11-12
11-13        *
12-13
13-14
13-9.3       *    
9.3-9.2      *
15,16,17-18  *
18-19
18-20        *
19-28
20-21        *
21-26        *
26-27        *
27-28        *
21-22.1
22.1-22.2
22.2-26
22.2-23
23-24
23-25
24-25
24-22.3
22.3-22.2       
25-22.3


5. Multiple Condition

if (user==null || user.getPassword()==null || user.getEmail()==null)
          T                X                          X  -> Frla RuntimeException so poraka:  "Mandatory information missing!"
	  F                T                          X  -> Frla RuntimeException so poraka:  "Mandatory information missing!"
	  F                F                          T  -> Frla RuntimeException so poraka:  "Mandatory information missing!"
	  F                F                          F  -> Prodolzuva normalno da se izvrsuva