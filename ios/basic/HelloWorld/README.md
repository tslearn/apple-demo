# 创建项目
### 1 创建 Single View Application
 ![image](https://github.com/tslearn/apple-demo/blob/master/ios/basic/HelloWorld/images/create/1.png)
### 2 将 General 配置下的 Main interface 设置为空
 ![image](https://github.com/tslearn/apple-demo/blob/master/ios/basic/HelloWorld/images/create/2.png)
### 3 修改 AppDelegate.m 中的 didFinishLaunchingWithOptions 方法
```smalltalk
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    // Override point for customization after application launch.
    self.window = [[UIWindow new] initWithFrame:[[UIScreen mainScreen] bounds]];
    [self.window setRootViewController: [ViewController new]];
    [self.window makeKeyAndVisible];
    
    return YES;
}
```
### 4 修改 ViewController.m 中的 viewDidLoad 方法
```smalltalk
- (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.
    
    self.view.backgroundColor = [UIColor purpleColor];
    
    UILabel* label = [[UILabel alloc] initWithFrame:CGRectMake(100, 100, 100, 100)];
    label.backgroundColor=[UIColor redColor];
    label.textColor=[UIColor blackColor];
    label.text = @"Hello";
    [self.view addSubview:label];
}
```
# 运行