```ruby
s = '
+++++ +++++
[
  > +++++ +++++ + > +++++ +++++ +
  > +++++ +++++ > +++++ +++++
  <<<< -
]
> . > +++++ . >> ++ . < +++++ . < . > . < .
'

m=[p=n=0,0,0,0,0];c=-1;case s[c];when'>';p+=1;when'<';p-=1
when'+';m[p]+=1;when'-';m[p]-=1;when'.';print m[p].chr;when
'[';loop{;case s[c+=1];when'[';n+=1;when']';break if n==0;
n-=1;end;}if m[p]==0;when']';loop{;case s[c-=1];when']';n+=1
;when'[';break if n==0;n-=1;end;}if m[p]!=0;end while s[c+=1]
```
