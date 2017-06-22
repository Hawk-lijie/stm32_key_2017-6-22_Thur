# stm32_key_2017-6-22_Thur

    u8 KEY_Scan(u8 mode) //mode:0,不支持连续按;1,支持连续按;
    {
     static u8 key_up=1;
     if(mode==1) key_up=1;//支持连续按 
      if（key_up &&  KEY按下） 
      {
        delay_ms(10);//延时，防抖 
        key_up=0;//标记这次key已经按下 
        if(KEY确实按下)
        {
           return KEY_VALUE;
        }
       }else if(KEY没有按下)  key_up=1;
       return 没有按下 
     } 
