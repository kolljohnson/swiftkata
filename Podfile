# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'swiftkata' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  # Pods for swiftkata
  pod 'Swifter', '~> 1.3.3'
  pod 'Alamofire', '~> 4.7'
  pod 'XCTest-Gherkin'

  target 'swiftkataTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'swiftkataUITests' do
    inherit! :search_paths
    # Pods for testing
  end

  post_install do |installer|
  installer.pods_project.targets.each do |target|
    if target.name == 'Swifter'
      target.build_configurations.each do |config|
        config.build_settings['SWIFT_VERSION'] = '3.2'
      end
    end
  end
  end
end
