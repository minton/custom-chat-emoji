task default: %w[gen]

task :gen do
  repo = "https://raw.githubusercontent.com/minton/custom-slack-emoji/master/"
  File.open Dir.getwd + '/README.md', 'w' do |f|
    f.puts "# custom-slack-emoji"
    f.puts "Just some random collection"
    f.puts ""
    f.puts "|name|preview|"
    f.puts "|----|-------|"
    images = Dir.glob(Dir.getwd + "/*.{jpg,png,gif,jpeg}")
    images.each do |img|
      name = File.basename(img)
      f.puts "|#{name}|![#{name}](#{repo}#{name})|"
    end
    f.puts ""
    f.puts "# Contributing"
    f.puts ""
    f.puts "Have a cool image to add? **__Together we can change the world!__**"
    f.puts "* Fork repo"
    f.puts "* Add your image to the root"
    f.puts "* Run `Rake` to generate some previews"
    f.puts "* Open a pull request"
  end
end
