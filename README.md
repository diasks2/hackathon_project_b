# 1st Annual Hackathon Audio Files (Project B)

```ruby

male_25_words = []
male_62_words = []
female_24_words = []

files.each do |file|
  if file[:sex] == "male" && file[:age_in_months] == 62
    male_62_words << file[:word_phrase]
  elsif file[:sex] == "male" && file[:age_in_months] == 25
    male_25_words << file[:word_phrase]
  elsif file[:sex] == "female" && file[:age_in_months] == 24
    female_24_words << file[:word_phrase]
  end
end

puts "Female (24 months): #{female_24_words.join(", ")}"
puts "Count: #{female_24_words.length}"
puts "Male (25 months): #{male_25_words.join(", ")}"
puts "Count: #{male_25_words.length}"
puts "Male (62 months): #{male_62_words.join(", ")}"
puts "Count: #{male_62_words.length}"

```

## Example Pronunciations

+ [blue](https://en.wiktionary.org/wiki/File:en-us-blue.ogg)
+ [bus](https://en.wiktionary.org/wiki/File:en-us-bus.ogg)
+ [nose](https://en.wiktionary.org/wiki/File:en-us-nose.ogg)