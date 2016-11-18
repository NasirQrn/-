# -一些小程序知识

坑
IDE---微信开发者工具 0.10.102800（各种坑）
  1、点击事件bindtap中在ide中点击事件会执行 两次 （真机测试无问题）。
  




技巧

  1、获取真机情况---  wx.getSystemInfo
  例
   //生命周期函数-监听页面初次渲染完毕
  onReady:function(){
    var that = this;
     wx.getSystemInfo({
       success: function(res) {
         console.log("..................");
         console.log(res);
         
         that.setData({
            swiperHeight: (res.windowHeight-37)
         });
       }
     })
  }
