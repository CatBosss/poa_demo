# poa_demo
实现存证模块的功能，包括：创建存证；撤销存证。
为存证模块添加新的功能，转移存证，接收两个参数，一个是内容的哈希值，另一个是存证的接收账户地址。 

终端命令行
- 克隆代码 使用monthly-2021-12 tag的
git clone -b monthly-2021-12 --depth 1 https://github.com/substrate-developer-hub/substrate-node-template
- 编译代码 
cargo build --release
- 部署开启节点
./target/release/node-template --dev --tmp
![2](https://user-images.githubusercontent.com/102146042/179365462-74250993-1e46-420c-989b-7a70b412e8d8.png)


安装前端模板库
- 确认安装了node yarn， 如果没有安装需要安装
node --version
yarn --version
npm install -g yarn
- 克隆前端模板库
git clone https://github.com/substrate-developer-hub/substrate-front-end-template
cd substrate-front-end-template
yarn install	//安装前端模板的依赖项

启动前端模板
命令启动 yarn start
http://localhost:8000/
![7](https://user-images.githubusercontent.com/102146042/179365464-cf9dd887-a731-48ae-a977-5e54a54a4cbc.png)


在https://polkadot.js.org/apps/#explorer中测试
- 选择Development local node，127.0.0.1：9944，然后转换按钮
- 选择 开发者 - 链状态，选择poeModule，proofs(Bytes): Option<(AccountId32,u32)>，输入0x00，加号按钮
运行结果：
poeModule.proofs: Option<(AccountId32,u32)>
<none>
- 选择 开发者 - 交易，选择poeModule，createClaim(claim)，revokeClaim(claim)，transferClaim(claim, dest)
输入0x00，提交交易等操作
  
![4](https://user-images.githubusercontent.com/102146042/179365490-07792cbb-4347-4921-a9ce-4eea200d230b.png)
  
![5](https://user-images.githubusercontent.com/102146042/179365493-2d17f599-ae0f-469d-9142-4c0f886777ab.png)
  
![6](https://user-images.githubusercontent.com/102146042/179365495-6fa4f40f-ed3c-4335-b4c0-1a8b7672a5b5.png)

