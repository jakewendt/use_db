require(File.join(File.dirname(__FILE__), 'config', 'boot'))

require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

desc 'Generate documentation for the gem.'
Rake::RDocTask.new(:rdoc) do |rdoc|
	rdoc.rdoc_dir = 'rdoc'
	rdoc.title		= 'USE DB'
	rdoc.options << '--line-numbers' << '--inline-source'
	rdoc.rdoc_files.include('README')
	rdoc.rdoc_files.include('lib/**/*.rb')
end

require 'tasks/rails'

begin
	require 'jeweler'
	Jeweler::Tasks.new do |gem|
		gem.name = "jakewendt-use_db"
		gem.summary = %Q{Gem version of use_db rails plugin}
		gem.description = %Q{Gem version of use_db rails plugin}
		gem.email = "github@jake.otherinbox.com"
		gem.homepage = "http://github.com/jakewendt/use_db"
		gem.authors = ["David Stevenson","George 'Jake' Wendt"]
		# gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings

#		gem.files  = FileList['config/routes.rb']
#		gem.files += FileList['app/**/*.rb']
#		gem.files += FileList['app/**/*.erb']
		gem.files  = FileList['lib/**/*.rb']
		gem.files += FileList['lib/**/*.rake']
		gem.files += FileList['rails/init.rb']
		gem.files += FileList['generators/**/*']
		gem.files -= FileList['**/versions/*']

		gem.test_files = []
#		gem.test_files = FileList['test/**/*.rb']
#	DO NOT INCLUDE test_helper.rb
#		gem.test_files -= FileList['test/test_helper.rb']

		gem.add_dependency('rails', '~> 2')
		gem.add_dependency('jakewendt-rails_extension')
	end
	Jeweler::GemcutterTasks.new
rescue LoadError
	puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

