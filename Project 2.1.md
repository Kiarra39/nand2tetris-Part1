HDL Code:

Half Adder:

     CHIP HalfAdder {
    IN a, b;    
    OUT sum,    
        carry;  
    PARTS:
     And(a=a,b=b,out=carry);
    Xor(a=a,b=b,out=sum);
}

![image](https://github.com/user-attachments/assets/9151031c-c745-4897-b552-9a3b8b6e112c)

Full Adder:

    CHIP FullAdder {
    IN a, b, c;  
    OUT sum,     
        carry;  

    PARTS:
    HalfAdder(a=a,b=b,sum=sum1,carry=carry1);
    HalfAdder(a=c,b=sum1,sum=sum,carry=carry2);
    Or(a=carry1,b=carry2,out=carry);
}

![image](https://github.com/user-attachments/assets/b02ab0e0-ff87-4c9b-917c-aa28a1d574ed)
