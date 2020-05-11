# utl-reading-a-classic-text-file-with-header-and-mutiple-trailers
Reading a classic text file with header and mutiple trailers
    Reading a classic text file with header and mutiple trailers                                              
                                                                                                              
    github                                                                                                    
    https://tinyurl.com/yb2oako5                                                                              
    https://github.com/rogerjdeangelis/utl-reading-a-classic-text-file-with-header-and-mutiple-trailers       
                                                                                                              
    stackoverflow sas                                                                                         
    https://tinyurl.com/yb8l6mee                                                                              
    https://stackoverflow.com/questions/61655557/move-some-columns-from-a-row-into-a-new-row                  
                                                                                                              
    *_                   _                                                                                    
    (_)_ __  _ __  _   _| |_                                                                                  
    | | '_ \| '_ \| | | | __|                                                                                 
    | | | | | |_) | |_| | |_                                                                                  
    |_|_| |_| .__/ \__,_|\__|                                                                                 
            |_|                                                                                               
    ;                                                                                                         
                                                                                                              
    filename ft15f001 "d:/txt/hedTrl.txt";                                                                    
    parmcards4;                                                                                               
    01JAN2004|9 |185 |02FEB2005|27SEP2010|36 |10SEP2011|12DEC2020|16 |                                        
    31JAN2010|2 |351 |17FEB2015|27DEC2020|2 | | | |                                                           
    ;;;;                                                                                                      
    run;quit;                                                                                                 
                                                                                                              
    d:/txt/hedTrl.txt                                                                                         
    01JAN2004|9 |185 |02FEB2005|27SEP2010|36 |10SEP2011|12DEC2020|16 |                                        
    31JAN2010|2 |351 |17FEB2015|27DEC2020|2 | | | |                                                           
                                                                                                              
    *            _               _                                                                            
      ___  _   _| |_ _ __  _   _| |_                                                                          
     / _ \| | | | __| '_ \| | | | __|                                                                         
    | (_) | |_| | |_| |_) | |_| | |_                                                                          
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                         
                    |_|                                                                                       
    ;                                                                                                         
                                                                                                              
    WORK.WANT total obs=3                                                                                     
                                                                                                              
       date       cod    total    trailers       dx           dy       cd                                     
                                                                                                              
     01JAN2004     9      185         1       02FEB2005    27SEP201    36                                     
     01JAN2004     9      185         2       10SEP2011    12DEC202    16                                     
     31JAN2010     2      351         1       17FEB2015    27DEC202    2                                      
                                                                                                              
    *                                                                                                         
     _ __  _ __ ___   ___ ___  ___ ___                                                                        
    | '_ \| '__/ _ \ / __/ _ \/ __/ __|                                                                       
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                       
    | .__/|_|  \___/ \___\___||___/___/                                                                       
    |_|                                                                                                       
    ;                                                                                                         
                                                                                                              
    data want;                                                                                                
      infile "d:/txt/hedTrl.txt" delimiter='|';                                                               
      input date$9. cod$ total$ @;                                                                            
      do trailers=1 to 2;                                                                                     
         input dx$9. dy$ cd$ @;                                                                               
         output;                                                                                              
      end;                                                                                                    
    run;quit;                                                                                                 
                                                                                                              
                                                                                                              
