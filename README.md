## promise-all-await
promise.all解决多个await互不相干的接口请求

```javascript

async function init(id){
  const getUser = getUser(id) //请求一
  const getPost = getPost(id) //请求二
  //用 Promise.all() 同时发送两个请求
  try{
    const result = await Promise.all([getUser,getPost])
    const userRes = result[0]
    const postRes = result[1]
    console.log(result)
  }catch (err){
    console.log(err)
  }
}

```
