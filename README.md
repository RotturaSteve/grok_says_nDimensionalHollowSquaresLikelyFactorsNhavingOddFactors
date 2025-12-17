the non-problem but rather big add is that the corners EACH have 'd' value, grok agreed that was not entirely caught by ChatGPT and far from just being a game-saver it might be a serious leap which is what i figured


nonetheless...


a rounding up or down of circle area diameter is the Z value of (Z+k)(Z-k)=N

solution to factoring odd semiprime composites of product N having two of them, O(1):

factor = [ Z = <<floor OR ceil>> of ( sqrt(N/PI) ) ] + sqrt(N - Z^2);





details:
        Z = {floor OR ceil} of ( sqrt(N/PI) ) ;
        Z^2+Zk - kZ+k^2 == N
        k == L == sqrt( N - Z^2 );
        factor = (Z+k)
        factor2 = (Z-k)







getting you the hollow square (works for 187=11*19, 95=5*19, 2059=29*71):

EXAMPLES:


sqrt(187/3.141592) == floor(7.71517732136) == 7 ... * 2 == 14 == Z in the Z-2q+1 with UNKNOWN q==6 == L @ UNKNOWN L==3

        FOR REFERENCE: 14-12+1 == 3 == L
        
        (Z-k)(Z+k) == 187
        
        Z(Z+k) - k(Z+k) == Z^2+Zk - kZ+k^2 == 187
                            196 + 14k - k*14 + k^2 == 187
                            14k - k*14 + k^2 == [187-196 == -9]
                            
                            14k - k*14 + k^2 == |-9|  == [9 == k^2]
                            
                            k = sqrt(9) == 3 == L
                            
                    now have L,Z therefore as k==L, you can find factors just from knowing 
                    
                    Z==L+2q-1==14==floor(sqrt(N/PI)) after precluding ceil(sqrt(N/PI))
                    
                            

sqrt(95/3.141592) == ceil(5.49904041435) == 6 ... *2 == 12 == Z in the Z-2q+1 with UNKNOWN q==3 == L @ UNKNOWN L==7

        FOR REFERENCE: 12-6+1 == 7 == L
        
        (Z-k)(Z+k) == 95
        
        Z(Z+k) - k(Z+k) == Z^2+Zk - kZ+k^2 == 95
                            144 + 12k - k*12 + k^2 == 95
                            
                            12k - k*12 + k^2 == [95-144 == -49]
                            
                            12k - k*12 + k^2 == |-49|  == [49 == k^2]
                            
                            k = sqrt(49) == 7 == L
                            
                    now have L,Z therefore as k==L, you can find factors just from knowing 
                    
                    Z==L+2q-1==12==ceil(sqrt(N/PI)) after precluding floor(sqrt(N/PI))

                    
                    
sqrt(2059/3.141592) == ceil(25.6007823254) == 26 ... *2 == 52 == Z in the Z-2q+1 with q==? == L @ UNKNOWN L==k==21

    PRECLUDED CEIL
        (Z-k)(Z+k) == 2059        

        Z(Z+k) - k(Z+k) == Z^2+Zk - kZ+k^2 == 2059
                            2704 + 52k - k*52 + k^2 == 2059
                            
                            52k - k*52 + k^2 == [2059-2704 == -645]
                            
                            52k - k*52 + k^2 == |-645|  == [645 == k^2]
                            
                            k = sqrt(645) == 25.3968501984 == L
                            
                    now have L,Z therefore as k==L, you can find factors just from knowing 
                    
                    Z==L+2q-1==52==ceil(sqrt(N/PI)) after precluding floor(sqrt(N/PI))
                    
            **** THIS PRECLUDES USING CEILING FOR FUNCTION, NOW TRY FLOOR, WHICH WORKS... ****
                    
    --------
        sqrt(2059/3.141592) == ceil(25.6007823254) == 25 ... *2 == 52 == Z
        (Z-k)(Z+k) == 2059 

        Z(Z+k) - k(Z+k) == Z^2+Zk - kZ+k^2 == 2059
                            2500 + 50k - k*50 + k^2 == 2059
                            
                            50k - k*50 + k^2 == [2059-2500 == -441]
                            
                            50k - k*50 + k^2 == |-441|  == [441 == k^2]
                            
                            k = sqrt(441) == 21 == L
                            
                    now have L,Z therefore as k==L, you can find factors just from knowing 
                    
                    Z==L+2q-1==50==floor(sqrt(N/PI)) after precluding floor(sqrt(N/PI))
    
**derived Z == 50 + derived 21 == 71 == factored { since modulus division is zero 2059%71 @@  29*71==2059 **
    
                (VERIFIED FOR THIS NUMBER)
                
                
____________________________________________________
        
        
        
NOTES/REFERENCE:


    Z = 50 & k = 21 ; (Z - k) * (Z + k) == 2059 (factors 29 , 71 )                
    uint64_t N = 2059;  // 29*71==2059; // 
    uint64_t P = 29;    // 29*71==2059; //
    uint64_t Q = 71;    // 29*71==2059; //
    uint64_t k = 21;                // pretend we don't know this // k:21 == sqrt ( pow(Z:50,2) - N:2059 )  //
    uint64_t Z = 50;                // pretend we don't know this // ( Z:50-k:21 ) * (Z:50+k:21 ) == N:2059 //
                        
                        
                        
                        
                        
                        
                        
                        
                        
                        
