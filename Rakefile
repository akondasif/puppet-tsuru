require 'puppetlabs_spec_helper/rake_tasks'
require 'puppet-lint/tasks/puppet-lint'

PuppetLint.configuration.send('disable_80chars')
PuppetLint.configuration.send('disable_class_parameter_defaults')
PuppetLint.configuration.ignore_paths = [
	"spec/**/*.pp",
	"vendor/**/*.pp",
	"api/spec/**/*.pp",
	"base/spec/**/*.pp",
	"docker/spec/**/*.pp",
	"gandalf/spec/**/*.pp",
	"registry/spec/**/*.pp",
]

Rake::Task[:spec].enhance [:lint]
