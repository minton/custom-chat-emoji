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
  end
end
