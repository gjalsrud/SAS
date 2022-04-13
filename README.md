# SAS

data data1;
input x y z ni @@;
cards;
1 1 1 18  1 1 2 12 
1 2 1 12 1 2 2 8
2 1 1 2 2 1 2 8
2 2 1 8 2 2 2 32
; 
run;
proc freq data=data1;
weight ni;
tables x*y*z/cmh;
run;

data data2;
input x y z ni @@;
cards;
1 1 1 53 1 1 2 414
1 2 1 11 1 2 2 37
2 1 1 0 2 1 2 16
2 2 1 4 2 2 2 139
;
run;
proc freq data=data2;
weight ni;
tables x*y*z/cmh;
run;

data data3;
input x y z ni @@;
cards;
1 1 1 6 1 1 2 4
1 2 1 2 1 2 2 8
2 1 1 4 2 1 2 3
2 2 1 1 2 2 2 5
3 1 1 5 3 1 2 3 
3 2 1 3 3 2 2 6
;
run;
proc freq data=data3;
weight ni;
tables x*y*z/cmh;
run;
