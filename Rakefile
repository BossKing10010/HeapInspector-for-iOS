desc "Bootstraps the repo"
task :bootstrap do
  sh 'bundle'
  sh 'cd Example/HeapInspectorExample && bundle exec pod install'
end

desc "Runs the specs"
task :spec do
  sh 'xcodebuild -workspace Example/HeapInspectorExample/HeapInspectorExample.xcworkspace -scheme \'HeapInspectorExample\' test -sdk iphonesimulator | xcpretty -tc; exit ${PIPESTATUS[0]}'
end
