### 工程目的
---
该工程师为了记录怎么使用github，和如何使用git同步代码而生成的示例工程。

同时该工程产生还实现了如何使用https://jitpack.io/生成项目引用。

该工程可以通过https://bintray.com上传引用到jcenter。注意因为bintray的变更，使得多了一个组织字段需要加上

<pre>
bintray {
    user = /*properties.getProperty("bintray.user")*/
    key = /*properties.getProperty("bintray.apikey")*/
    configurations = ['archives']
    pkg {
        userOrg = "bimao"//特别注意点
        repo = "maven2"
        name = "MyLibrary"    //发布到JCenter上的项目名字
        websiteUrl = siteUrl
        vcsUrl = gitUrl
        licenses = ["Apache-2.0"]
        publish = true
    }
}
</pre>

