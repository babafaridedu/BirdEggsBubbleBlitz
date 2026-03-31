platform :ios, '14.0'

target 'ChickenEggs BubbleBlitz' do
  use_frameworks!

  pod 'Skillz', '2025.0.50'
end

post_install do |installer|
  bitcode_strip_path = `xcrun --find bitcode_strip`.chomp

  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '14.0'
      config.build_settings['BUILD_LIBRARY_FOR_DISTRIBUTION'] = 'YES'
      config.build_settings['GCC_TREAT_WARNINGS_AS_ERRORS'] = 'NO'
      config.build_settings['SWIFT_TREAT_WARNINGS_AS_ERRORS'] = 'NO'
    end
  end
end