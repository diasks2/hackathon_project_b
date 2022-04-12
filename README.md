# 1st Annual Hackathon Audio Files (Project B)

```ruby

male_25_words = []
male_62_words = []

files.each do |file|
  if file[:sex] == "male" && file[:age_in_months] == 62
    male_62_words << file[:word_phrase]
  elsif file[:sex] == "male" && file[:age_in_months] == 25
    male_25_words << file[:word_phrase]
  end
end

puts "Male (25 months): #{male_25_words.join(", ")}"
puts "Count: #{male_25_words.length}"
puts "Male (62 months): #{male_62_words.join(", ")}"
puts "Count: #{male_62_words.length}"

```