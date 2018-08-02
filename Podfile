# Uncomment the next line to define a global platform for your project
platform :ios, '9.3'

target 'swiftkata' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  # Pods for swiftkata
  def core_pods
    pod 'Swifter', '~> 1.3.3'
    pod 'Alamofire', '~> 4.7'
  end

  def testing_pods
    pod 'XCTest-Gherkin'
  end

  core_pods
  
  target 'swiftkataTests' do
    inherit! :search_paths
    # Pods for testing
    core_pods
    testing_pods
  end

  target 'swiftkataUITests' do
    inherit! :search_paths
    # Pods for testing
    core_pods
    testing_pods
  end

  post_install do |installer|
  installer.pods_project.targets.each do |target|
    if target.name == 'Swifter'
      target.build_configurations.each do |config|
        config.build_settings['SWIFT_VERSION'] = '3.2'
      end
    end
  end
    # Workaround for Cocoapods issue #7606
  installer.pods_project.build_configurations.each do |config|
        config.build_settings.delete('CODE_SIGNING_ALLOWED')
        config.build_settings.delete('CODE_SIGNING_REQUIRED')
    end
  end
end
