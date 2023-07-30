```ruby
MyName = "nsfisis"

ss = [
  "GHlBH", "2,a0KLG", "Rc1_g",
  "![oLhVE", "2,a0KLG",
  "![oLhVE", "2,a0KLG",
]

puts ss
  .map{|s| s
    .each_char
    .map{(_1.ord + 12323).chr(Encoding::UTF_8)}
    .join}
  .zip(MyName.each_char)
  .map{"#{_2} | #{_1}"}
```
