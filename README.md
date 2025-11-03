


# Install dependencies

```shell
# Python version： 3.10
pip install -r requirements.txt
```

# Startup program

```text
Execute the main function in graph_builder within agent_graph.
```


```text
                          +-----------+                           
                          | __start__ |                           
                          +-----------+                           
                                 *                                
                                 *                                
                                 *                                
                       +-----------------+                        
                       | classify_intent |                        
                       +-----------------+..                      
                          ..                ....                  
                        ..                      ....              
                      ..                            ....          
               +--------+                               ...       
               | detect |                                 .       
               +--------+                                 .       
                    *                                     .       
                    *                                     .       
                    *                                     .       
            +--------------+                              .       
            | generate_sql |                              .       
            +--------------+                              .       
                    *                                     .       
                    *                                     .       
                    *                                     .       
             +------------+                               .       
             | sql_router |                               .       
             +------------+                               .       
             ...          ..                              .       
            .               ..                            .       
          ..                  ..                          .       
+-------------+          +---------------+          +----------+  
| execute_sql |          | filter_result |          | llm_chat |  
+-------------+          +---------------+          +----------+  
                                       ***         ***            
                                          *       *               
                                           **   **                
                                        +---------+               
                                        | __end__ |               
                                        +---------+               

```