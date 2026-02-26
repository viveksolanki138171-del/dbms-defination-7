# dbms-defination-7
--Write a PL/SQL block to accept product name, qty and price from user and then calculate discount in Rs. based on the given (%).

set serveroutput on; declare
v_pname		varchar2(50); v_qty	 number; v_price		number; v_percent number; v_total	number; v_discount number;

begin

v_pname		:= '&enter_product_name'; v_qty	:= &enter_quantity;
v_price	:= &enter_price;
v_percent := &enter_discount_percent;

v_total := v_qty * v_price;
v_discount := (v_total * v_percent) / 100;

dbms_output.put_line('product name : ' || v_pname); dbms_output.put_line('total amount : ' || v_total); dbms_output.put_line('discount (rs): ' || v_discount);

end;
/
