Actual output:

$ bundle exec rake spec
/usr/bin/ruby -I/home/ekohl/.gem/ruby/gems/rspec-core-3.5.4/lib:/home/ekohl/.gem/ruby/gems/rspec-support-3.5.0/lib /home/ekohl/.gem/ruby/gems/rspec-core-3.5.4/exe/rspec --pattern spec/\{aliases,classes,defines,unit,functions,hosts,integration,types\}/\*\*/\*_spec.rb --color
F

Failures:

  1) example should compile into a catalogue without dependency cycles
     Failure/Error: it { is_expected.to compile.with_all_deps }
       error during compilation: Validation of Exec[openssl] failed: 'openssl' is not qualified and no path was specified. Please qualify the command or specify a path. at /home/ekohl/dev/example/spec/fixtures/modules/example/manifests/init.pp:2
     # ./spec/classes/example_spec.rb:4:in `block (2 levels) in <top (required)>'

Finished in 0.39062 seconds (files took 0.80743 seconds to load)
1 example, 1 failure

Failed examples:

rspec ./spec/classes/example_spec.rb:4 # example should compile into a catalogue without dependency cycles

/usr/bin/ruby -I/home/ekohl/.gem/ruby/gems/rspec-core-3.5.4/lib:/home/ekohl/.gem/ruby/gems/rspec-support-3.5.0/lib /home/ekohl/.gem/ruby/gems/rspec-core-3.5.4/exe/rspec --pattern spec/\{aliases,classes,defines,unit,functions,hosts,integration,types\}/\*\*/\*_spec.rb --color failed
