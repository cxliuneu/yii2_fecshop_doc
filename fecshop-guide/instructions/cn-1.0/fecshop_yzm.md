Fecshop验证码
============

> 在注册账户，登录，找回密码等表单提交的地方需要验证码，
> 您可以通过配置的方式决定是否开启验证码。

配置文件为：`@fecshop/app/appfront/config/modules/Customer.php`

打开后通过注释就可以找到各个配置项.


```
return [
	'customer' => [
		'class' => '\fecshop\app\appfront\modules\Customer\Module',
		'params'=> [
			'register' => [
				# 账号注册成功后，是否自动登录
				'successAutoLogin' => true, 
				# 注册登录成功后，跳转的url
				'loginSuccessRedirectUrlKey' => 'customer/account', 
				# 注册页面的验证码是否开启
				'registerPageCaptcha' => true, 
				
			],
			'login' => [
				# 在登录页面 customer/account/login 页面登录成功后跳转的urlkey，
				'loginPageSuccessRedirectUrlKey' => 'customer/account',
				# 在其他页面的弹框方式登录的账号成功后，的页面跳转，如果是false，则代表返回原来的页面。
				'otherPageSuccessRedirectUrlKey' => false  ,
				# 登录页面的验证码是否开启
				'loginPageCaptcha' => false,  
				# 邮件信息，登录账号后是否发送邮件
				
			],
			'forgotPassword' => [
				# 忘记密码页面的验证码是否开启
				'forgotCaptcha' => true, 
				
			],
			
			'leftMenu'  => [
				'Account Dashboard' => 'customer/account',
				'Account Information' => 'customer/editaccount',
				'Address Book' => 'customer/address',
				'My Orders' => 'customer/order',
				'My Product Reviews' => 'customer/productreview',
				'My Favorite' => 'customer/productfavorite',
				
			],
			
			'contacts'	=> [
				# 联系我们页面的验证码是否开启
				'contactsCaptcha' => true, 
				
			],
			'newsletterSubscribe' => [
				
			],
		],
	],
];
```

您可以在appfront通过添加配置覆盖的方式，重新设置是否开启验证码。






























