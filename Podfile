source 'http://lvioscode.com/ios_pods_specs/Specs.git'
source 'https://github.com/CocoaPods/Specs.git'

platform :ios, '8.0'

target 'CallCenterSwift' do
    use_frameworks!

    pod 'MJRefresh', '1.4.401'
    pod 'FTUtils', :git => 'http://lvioscode.com/ios_vendor/ftutils.git', :branch => '1.1.11'
        pod 'LvmmBaseClass', :git => 'http://lvioscode.com/ios_pods_business_lvmama/LvmmBaseClass.git', :branch => '1.2.6'
    pod 'LvmmCategory', :git => 'http://lvioscode.com/ios_pods_kit/LvmmCategory.git', :branch => '1.0.9'
    pod 'LvmmCms', :git => 'http://lvioscode.com/ios_pods_business_lvmama/LvmmCms.git', :branch => '1.0.3'
    pod 'LvmmCommonView',  :git => 'http://lvioscode.com/ios_pods_kit/LvmmCommonView.git', :branch => '2.0.5'
    pod 'LvmmConfig', :git => 'http://lvioscode.com/ios_pods_business_lvmama/LvmmConfig.git', :branch => '1.2.6'
    pod 'LvmmImage', :git => 'http://lvioscode.com/ios_pods_kit/LvmmImage.git', :branch => '1.0.4'
    pod 'LvmmLocation',  '1.1.1'
    pod 'LvmmMediator', :git => 'http://lvioscode.com/ios_pods_business_lvmama/LvmmMediator.git', :branch => '1.0.6'
    pod 'LvmmNetwork', :git => 'http://lvioscode.com/ios_pods_function/LvmmNetwork.git', :branch => '3.0.4'
    pod 'LvmmShare', :git => 'http://lvioscode.com/ios_pods_function/LvmmShare.git', :branch => '1.1.2'
    pod 'LvmmStatistics', :git => 'http://lvioscode.com/ios_pods_function/LvmmStatistics.git', :branch => '1.1.6'
    pod 'LvmmUtil',  :git => 'http://lvioscode.com/ios_pods_kit/LvmmUtil.git', :branch => '1.0.5'
    target 'CallCenterSwiftTests' do
        inherit! :search_paths
    end
    post_install do |installer|
        installer.pods_project.targets.each do |target|
            target.build_configurations.each do |config|
                config.build_settings['ENABLE_BITCODE'] = 'NO'
                config.build_settings['CLANG_ALLOW_NON_MODULAR_INCLUDES_IN_FRAMEWORK_MODULES'] = 'YES'
                if config.name == 'Debug'
                    config.build_settings['GCC_PREPROCESSOR_DEFINITIONS'] = 'POD_CONFIGURATION_DEBUG=1', 'DEBUG=1','USE_FRAMEWORK'
                end
                if config.name == 'Release'
                    config.build_settings['GCC_PREPROCESSOR_DEFINITIONS'] = 'POD_CONFIGURATION_RELEASE=1','USE_FRAMEWORK'
                end
            end
        end
    end
end
