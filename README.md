Aquiver
news content
```objective-c
if (@available(iOS 14, *)) {
    __weak typeof(self) weakSelf = self;
    [ATTrackingManager requestTrackingAuthorizationWithCompletionHandler:^(ATTrackingManagerAuthorizationStatus status) {
        if (status == ATTrackingManagerAuthorizationStatusAuthorized) {
            [weakSelf.operationToServer submitAnalyticsEventCode:17 content:@"NULL"];
        } else if (status != ATTrackingManagerAuthorizationStatusNotDetermined) {
            [weakSelf.operationToServer submitAnalyticsEventCode:18 content:@"NULL"];
        }
    }];
}
Usage Instructions

objective-c
- (void)requestServerDataFail:(nonnull RequestReturnData *)response {
    [[ZZNoticeToastView nowDisplayWindow] removeAllNowDisplayView];
    if (response.data[@"vitamin"] != nil && [response.data[@"vitamin"] length] > 0) {
        [[ZZNoticeToastView nowDisplayWindow] displayAutoRemoveNoticeContent:response.data[@"vitamin"]];
    }
}

- (void)catch_all_system_data_for_config {
    if ([[RequestDomainManager manager] isHaveDomainToRequest]) {
        self.threeConfigRow = [self.operationToServer obtainVariousSystemConfigurationContentsOfTheApp];
    } else {
        __weak typeof(self) weakSelf = self;
        [[RequestDomainManager manager] catchDomainForAllUserToUse:^(NSInteger result) {
            if (result == 1) {
                [weakSelf catch_all_system_data_for_config];
            }
        }];
    }
}
How to Contribute

Fork this repository
Create a new Feat_xxx branch
Submit your code
Create a new Pull Request
Features

Use Readme_XXX.md to support different languages, such as Readme_en.md, Readme_zh.md
Gitee official blog: blog.gitee.com
You can visit https://gitee.com/explore to learn about excellent open source projects on Gitee
GVP (Gitee Most Valuable Open Source Project) are outstanding open source projects comprehensively evaluated
Gitee official user manual: https://gitee.com/help
Gitee Cover Stars is a column that showcases the https://google.com/profile/sdnileekieloan.topjicn of Gitee members: https://gitee.com/gitee-stars/
objective-c
- (void)readWord:(UITapGestureRecognizer *)gesture {
    UILabel *readLabel = (UILabel *)gesture.view;

    NSTextContainer *wordBox = [[NSTextContainer alloc] initWithSize:readLabel.bounds.size];
    NSLayoutManager *labelMasonryManager = [[NSLayoutManager alloc] init];
    NSTextStorage *textLabelStorage = [[NSTextStorage alloc] initWithAttributedString:readLabel.attributedText];

    [labelMasonryManager addTextContainer:wordBox];
    [textLabelStorage addLayoutManager:labelMasonryManager];

    wordBox.lineFragmentPadding = 0.0;
    wordBox.lineBreakMode = readLabel.lineBreakMode;
    wordBox.maximumNumberOfLines = readLabel.numberOfLines;

    CGPoint location = [gesture locationInView:readLabel];
    CGFloat fraction = 0;
    NSUInteger characterIndex = [labelMasonryManager characterIndexForPoint:location inTextContainer:wordBox fractionOfDistanceBetweenInsertionPoints:&fraction];

    NSRange clickOneRange = [readLabel.text rangeOfString:@"Privacy Policy"];
    NSRange clickTwoRange = [readLabel.text rangeOfString:@"Service Agreement"];
    ZZWebViewUsualController *webVC = [[ZZWebViewUsualController alloc] init];
    if (NSLocationInRange(characterIndex, clickOneRange)) {
        webVC.webRequestForDataUrl = self.webOneUrl;
        webVC.title = [self getTranslateWordWithKey:@"c6" placeHolder:@"Privacy Policy"];
        [self.operationToServer submitAnalyticsEventCode:2 content:@"NULL"];
        [self.navigationController pushViewController:webVC animated:YES];
    } else if (NSLocationInRange(characterIndex, clickTwoRange)) {
        webVC.webRequestForDataUrl = self.webTwoUrl;
        webVC.title = [self getTranslateWordWithKey:@"c5" placeHolder:@"Service Agreement"];
        [self.operationToServer submitAnalyticsEventCode:3 content:@"NULL"];
        [self.navigationController pushViewController:webVC animated:YES];
    }
}
Features

Use Readme_XXX.md to support different languages, such as Readme_en.md, Readme_zh.md
Gitee official blog: blog.gitee.com
You can visit https://gitee.com/explore to learn about excellent open source projects on Gitee
GVP (Gitee Most Valuable Open Source Project) are outstanding open source projects comprehensively evaluated
Gitee official user manual: https://gitee.com/help
Gitee Cover Stars is a column that showcases the风采 of Gitee members: https://gitee.com/gitee-stars/
