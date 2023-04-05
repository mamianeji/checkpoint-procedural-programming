# checkpoint-procedural-programming
FUNCTION dot_product(v1,v2) : INTEGER
VAR
        ps:INTEGER
        i:INTEGER;
BEGIN
    ps:=0;
    FOR i FROM 0 TO v1.length  STEP step  DO
        ps:=ps+(v1[i]*v2[i])
    END_FOR
    RETURN ps ;
END

ALGORITHM product_using_function
VAR
  v1 : ARRAY_OF INTEGER [10];
  v2 : ARRAY_OF INTEGER [10];
  k,i,j,res:INTEGER;
 
BEGIN
    write("give the numbers of pairs couples")
    read(n)

FOR k FROM 0 TO n-1 STEP step  DO

    FOR i FROM 0 TO 11 STEP step  DO
        read(v1[i])
    END_FOR
    FOR j FROM 1 TO 11 STEP step  DO
        read(v2[j])
    END_FOR
    res=dot_product(v1,v2)
    
    IF (res=0) THEN
        write("the vectors are orthogonal")
    ELSE
       write("the vectors are not orthogonal")
    END_IF

END_FOR

END
