# aws-lambda-php-sam

aws lambda + php + sam-cli

## 事前に必要なもの

* AWS CLI already configured with Administrator permission
* [Docker installed](https://www.docker.com/community-edition)
* SAM CLI - [Install the SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)

## 使い方

### Installing dependencies & building the target 

In this example we use the built-in `sam build` to build a docker image from a Dockerfile and then copy the source of your application inside the Docker image.  
Read more about [SAM Build here](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/sam-cli-command-reference-sam-build.html) 

### Local development

**Invoking function locally through local API Gateway**

```bash
sam build
sam local start-api
```

## Packaging and deployment

To deploy your application for the first time, run the following in your shell:

```bash
sam deploy --guided
```

### Testing

準備中

## TODO

- [X] `sam build`でphp実行コンテナをビルドできるように
- [ ] composer.json を用意してコンテナビルド内でcomposer installするように
- [ ] phpunitを用意する
- [ ] codebuildでデプロイできるように

## 参考資料

- 元々これを参考に作成しました, https://aws.amazon.com/jp/builders-flash/202107/new-lambda-container-development-4/?awsf.filter-name=*all