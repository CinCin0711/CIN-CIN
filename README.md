using System;
using System.Collections.Generic;

namespace pt2
{
    class Program
    {
        static void Main(string[] args)
        {
            string loai_tien = "";
            string hinh_thuc = "";
            int tien = 0, kq = 0;
            Console.WriteLine("nhap loai tien:");
            loai_tien = Console.ReadLine();
            Console.WriteLine("nhap so tien");
            tien = int.Parse(Console.ReadLine());
            Console.WriteLine("nhap hinh thuc trao doi");
            hinh_thuc = Console.ReadLine();
            if (tien < 0)
            {
                Console.WriteLine("nhap sai tien!");
            }
            else
            { switch (loai_tien)
                {
                    case "usd":
                        switch (hinh_thuc)
                        {
                            case "mua":
                                kq = tien * 19000;
                                Console.WriteLine("So tien VN phair tra la {0} khi mua usd:", kq);
                                break;
                            case "ban":
                                kq = tien * 17500;
                                Console.WriteLine("So tien VN cos duoc la {0} khi ban usd:", kq);
                                break;
                        }
                    case "euro":
                        switch (hinh_thuc)
                        {
                            case "mua":
                                kq = tien * 24500;
                                Console.WriteLine("So tien VN phair tra la {0} khi mua euro:", kq);
                                break;
                            case "ban":
                                kq = tien * 23500;
                                Console.WriteLine("So tien VN cos duoc la {0} khi ban euro:", kq);
                                break;
                        }
                    case "yen":
                        switch (hinh_thuc)
                        {
                            case "mua":
                                kq = tien * 1300;
                                Console.WriteLine("So tien VN phair tra la {0} khi mua yen:", kq);
                                break;
                            case "ban":
                                kq = tien * 1250;
                                Console.WriteLine("So tien VN cos duoc la {0} khi ban yen", kq);
                                break;
                        }
                }

            }
        
            Console.ReadLine();
        }
    }
}
