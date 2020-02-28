# Resume

## Dubkovskaya Tatiana 

Contacts:
* @ovalski – telegram
* tanya.kavretskaya@mail.ru – email
* 375 33 649 25 84 – phone

My current goal is to become an android developer, who can work both with orders and my own apps. I enjoy to create something for myself, for my own goals, but I also a team player, so I would like to work in a group, participate in extensive projects, be able to share ideas and enrich my skills during work with command. Mobile development is not the only thing which I’m interested in. I also excited of artificial intelligence, and in the future I want to combine those hobbies. 

My main language is c#. I have been working with it for 1.5 years. Before it I was learning c++ during 1 year at the university and by myself, when education program was not enough. Now I’m working with Xamarin Android for several months. 

Last thing I do was short piece of code not for mobile, but for desktop app. It was made for person, who needs to create white fields around photos for Instagram. Now I’m writing a mobile version. 

        using System;
        using System.Drawing;
        using System.Drawing.Imaging;
        using System.Collections.Generic;

        namespace ForCheck
        {
            class Program
            {
                static void Main(string[] args)
                {
                    var name = Console.ReadLine();
                    CreateFields(name);
                    Console.WriteLine("done");
                    Console.ReadKey();
                }

                public static void CreateFields( string path)
                {
                    Image source = Bitmap.FromFile(path);

                    int h = source.Height;
                    int w = source.Width;
                    source.Save(Environment.GetFolderPath(Environment.SpecialFolder.Desktop) + "\\1.jpg");
                    var newW = 4 * h / 5;  //новая ширина
                    var t = (newW - w) / 2;  //каждая сторона

                    Image left = new Bitmap(t, h);
                    using (Graphics grp = Graphics.FromImage(left))
                    {
                        grp.FillRectangle(
                            Brushes.White, 0, 0, t, h);
                    }

                    Bitmap resultImage = new Bitmap(newW, h);

                    using (Graphics g = Graphics.FromImage(resultImage))
                    {
                        g.DrawImage(left, 0, 0, left.Width, left.Height);
                        g.DrawImage(source, left.Width, 0, w, h);
                        g.DrawImage(left, source.Width + left.Width, 0, newW, h);
                    }
                    resultImage.Save(Environment.GetFolderPath(Environment.SpecialFolder.Desktop) + "\\white.jpg");
                }
            }
        }


As for work experience, I didn’t have any large-scale projects to talk about. I’m learning by myself or on online courses, so I have only homework or tasks from my friends. I pass tests and got into Itransition courses last year, but my studying wasn’t enough successful. 

I have been studying at the Belarusian State University of Informatic and Radioelectronic for 3 years. I watched online c# courses on Coursera and lectures on ITVDN and Youtube channels like SimpleCode, Byte++, Code Blog, Joe Rock.

I was learning English since primary school, was continuing my education on gymnasium with English bias, so after graduating my language level was high enough. But during studying at the university it fell down. Now I can read and understand, but my grammar and accent are not really good.  I failed this test and my result was A2, but usually it’s between B1 and B2.