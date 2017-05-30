source 'https://github.com/CocoaPods/Specs.git'
source 'https://github.com/artsy/Specs.git'

plugin 'cocoapods-keys', {
  :project => 'Eidolon',
  :keys => [
    'ArtsyAPIClientSecret',
    'ArtsyAPIClientKey',
    'HockeyProductionSecret',
    'HockeyBetaSecret',
    'SegmentWriteKey',
    'CardflightProductionAPIClientKey',
    'CardflightProductionMerchantAccountToken',
    'StripeProductionPublishableKey',
    'CardflightStagingAPIClientKey',
    'CardflightStagingMerchantAccountToken',
    'StripeStagingPublishableKey'
  ]
}

platform :ios, '10.0'
use_frameworks!

# Yep.
inhibit_all_warnings!

target 'Kiosk' do

  # Artsy stuff
  pod 'Artsy+UIColors'
  pod 'Artsy+UILabels'
  pod 'Artsy-UIButtons'

  if ENV['ARTSY_STAFF_MEMBER'] != nil || ENV['CI'] != nil
      pod 'Artsy+UIFonts'
  else
      pod 'Artsy+OSSUIFonts'
  end

  pod 'ORStackView', '2.0'
  pod 'FLKAutoLayout', '0.1.1'
  pod 'ARCollectionViewMasonryLayout', '~> 2.0.0'
  pod 'SDWebImage', '~> 3.7'
  pod 'SVProgressHUD'

  pod 'ARAnalytics/Segmentio'
  pod 'ARAnalytics/HockeyApp'

  pod 'CardFlight', '3.2.1'
  pod 'Stripe'
  pod 'ECPhoneNumberFormatter'
  pod 'UIImageViewAligned', :git => 'https://github.com/ashfurrow/UIImageViewAligned.git'
  pod 'DZNWebViewController', :git => 'https://github.com/orta/DZNWebViewController.git'
  pod 'ReachabilitySwift'

  pod 'UIView+BooleanAnimations'
  pod 'ARTiledImageView'
  pod 'XNGMarkdownParser'
  pod 'ISO8601DateFormatter'

  # Swift pods
  pod 'SwiftyJSON'
  pod 'RxSwift'
  pod 'RxCocoa'
  pod 'Moya/RxSwift'
  pod 'NSObject+Rx'
  pod 'Action'

  target 'KioskTests' do
    inherit! :search_paths

    pod 'FBSnapshotTestCase'
    pod 'Nimble-Snapshots'
    pod 'Quick'
    pod 'Nimble'
    pod 'Forgeries'
    pod 'RxBlocking'

  end
end
