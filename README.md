# DigitNegativeLibrary
Create by : Денис Казанцев & Артем Николаев

-lib

    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    
    namespace DigitNegativeLibrary
    {
        public class DigitNegative
        {
            int[] num = new int[10];
            public static int DivNegative1(int[] num) 
            {
                int a = 1;
                for( int i = 0; i < num.Length; i++)
                {
                    int zxc = num[i];
                    if (zxc == num.Max())
                    {
                        i ++;
                        while (i<num.Length)
                        {
                            a *= num[i];
                            i++;
                        }
                    }
    
                }
                return a;
            }
        }
        public class DigitRigth
        {
            public static int Rightmoment(int[] num)
            {
                int zov = 0;
                Array.Sort(num);
                return zov;
            }
        }
    }

-Test

    using Microsoft.VisualStudio.TestTools.UnitTesting;
    using System;
    using DigitNegativeLibrary;
    
    namespace DigitNegativeTests
    {
        [TestClass]
        public class DigitNegativeTests
        {
            [TestMethod]
            public void TestMethod1()
            {
                // Arrange
                int[] num = { 1, 2, -2, 4, 5, -6, -7, -8, -9, -10 };
                int actual = DigitNegative.DivNegative1(num);
                Assert.AreEqual(-30240, actual);
            }
        }
    }


