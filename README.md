# bluewhale

## Table Of Contents

- [How to use](#how-to-use)
- [How to contribute](#how-to-contribute)
- [License](#license)




## How to use

Assuming you have [Ruby](https://www.ruby-lang.org/en/downloads/) and [Bundler](https://bundler.io/) installed on your system (*hint: for ease of managing ruby gems, consider using [rbenv](https://github.com/rbenv/rbenv)*), first [fork](https://guides.github.com/activities/forking/) the theme from `github.com:BlueWhaleLab/bluewhalelab.github.io` to `github.com:<your-username>/<your-repo-name>` and do the following:

```bash
$ git clone git@github.com:<your-username>/<your-repo-name>.git
$ cd <your-repo-name>
$ bundle install
$ bundle exec jekyll serve
```

Then, feel free to customize the theme however you like (don't forget to change the name!).
After you are done, **commit** your final changes.

## How to contribute 

Contributing to the Blog Locally (Taking macOS as an example):

1. Ensure Ruby and Bundler are installed on your local environment
2. Clone the repository to your local machine:
   ```bash
   $ git clone git@github.com:BlueWhaleLab/bluewhalelab.github.io.git
   $ cd bluewhalelab.github.io
   ```
4. Create a new blog post in the `_posts` directory with the filename format `YYYY-MM-DD-title.md`
5. Add YAML front matter at the beginning of the file:
   ```yaml
   ---
   layout: post
   title: Your Blog Title
   date: YYYY-MM-DD HH:MM:SS +/-TTTT
   categories: category
   tags: tag1 tag2
   ---
   ```
6. Write your blog content using Markdown format
7. Preview the blog locally:
   ```bash
   $ bundle exec jekyll serve --incremental
   ```
8. Visit `http://localhost:4000` in your browser to see the result
9. Before submitting changes, ensure your branch is up-to-date:
   ```bash
   $ git pull origin main
   ```
   If there are conflicts, resolve them before continuing.

10. Once confirmed, commit your changes:
    ```bash
    $ git add .
    $ git commit -m "Add new blog post"
    $ git push origin main
    ```

11. Create a Pull Request to the main repository:
    - Visit your repository page on GitHub
    - Click the "Pull requests" tab
    - Click the "New pull request" button
    - Ensure the "base repository" is the main repository and "base" branch is main
    - Ensure the "head repository" is your repository and "compare" branch is your modified branch
    - Add a clear title and description explaining your changes
    - Click the "Create pull request" button

12. Wait for repository maintainers to review your Pull Request:
    - If there are suggestions for modifications, make adjustments based on feedback
    - Once approved, your changes will be merged into the main repository

中文： 
在本地（以macbook举例） 

1. 确保你的本地环境已经安装了 Ruby 和 Bundler
2. 克隆仓库到本地：
   ```bash
   $ git clone git@github.com:BlueWhaleLab/bluewhalelab.github.io.git
   $ cd bluewhalelab.github.io
   ```
4. 在 `_posts` 目录下创建新的博客文章，文件名格式为 `YYYY-MM-DD-title.md`
5. 在文件开头添加 YAML 头信息：
   ```yaml
   ---
   layout: post
   title: 你的博客标题
   date: YYYY-MM-DD HH:MM:SS +/-TTTT
   categories: 分类
   tags: 标签1 标签2
   ---
   ```
6. 使用 Markdown 格式编写博客内容
7. 本地预览博客：
   ```bash
   $ bundle exec jekyll serve  --incremental 
   ```
8. 在浏览器中访问 `http://localhost:4000` 查看效果
9. 在提交更改前，确保你的分支是最新的：
   ```bash
   $ git pull origin main
   ```
   如果有冲突，请解决冲突后再继续。

10. 确认无误后，提交更改：
    ```bash
    $ git add .
    $ git commit -m "添加新的博客文章"
    $ git push origin main
    ```

11. 创建 Pull Request 到主仓库：
    - 访问 GitHub 上你的仓库页面
    - 点击 "Pull requests" 选项卡
    - 点击 "New pull request" 按钮
    - 确保"base repository"是主仓库，"base"分支是main
    - 确保"head repository"是你的仓库，"compare"分支是你的修改分支
    - 添加清晰的标题和描述，说明你的更改内容
    - 点击 "Create pull request" 按钮

12. 等待仓库维护者审核你的 Pull Request：
    - 如果有修改建议，请根据反馈进行调整
    - 审核通过后，你的更改将被合并到主仓库

## License

The theme is available as open source under the terms of the [MIT License](https://github.com/alshedivat/al-folio/blob/main/LICENSE).

Originally, **al-folio** was based on the [\*folio theme](https://github.com/bogoli/-folio) (published by [Lia Bogoev](https://liabogoev.com) and under the MIT license). Since then, it got a full re-write of the styles and many additional cool features.
