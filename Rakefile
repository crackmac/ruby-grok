task :default => [:package]

task :package do
  system("gem build grok.gemspec")
end

task :publish do
  latest_gem = %x{ls -t jls-grok*.gem}.split("\n").first
  system("gem push #{latest_gem}")
end
