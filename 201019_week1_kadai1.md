def compute_sorori_shinzaemon(day=100):
    """
    曽呂利新左衛門の米の逸話を検証する関数。日にちごとの米の粒の数を計算する。

    Parameteres
    --------------
    day: int
        米を貰う日数 (default : 100)

    Returns
    --------------
    list_n_grains : list
        ある日に貰う米の数のリスト（リストの長さはdayに等しくなる）
    list_total_grains : list
        ある日までに累計で貰う米の数のリスト（リストの長さはdayに等しくなる）
    """
    # ここにコードを書く。passは何もしないことを意味する命令である。
    pass
    return list_n_grains, list_total_grains
#list_n_grains, list_total_grains = compute_sorori_shinzaemon(day=10)

list_n_grains = []
#print(list_n_grains)
#print(len(list_n_grains))

list_total_grains = []
print(list_total_grains)
print(len(list_total_grains))

#day = float(input())

day = 80
people = 2
one_day_grains = 14000

n_grains = 1
total_grains = 0

for num in range(0,day):
   total_grains = total_grains + n_grains
   list_n_grains.append(n_grains)
   list_total_grains.append(total_grains)
   n_grains = n_grains * 2

one_day_grains_my_home = people * one_day_grains
print( '１日あたり家で消費するコメの量は' + str(one_day_grains_my_home) + '粒です' )

how_many_days_we_can_alive = (list_total_grains[-1]) // one_day_grains_my_home
print(list_total_grains[-1])
print(how_many_days_we_can_alive)

print("私たちが生きれるのは" + str(how_many_days_we_can_alive) + "日です")
print("私たちが生きれるのは" + str((how_many_days_we_can_alive) //365) + "年です")


import matplotlib.pyplot as plt
%matplotlib inline
plt.title("Sororishinzaemon's Kome,fes!")
plt.xlabel("days")
plt.ylabel("kome-tsubu")
plt.plot(list_n_grains) # 「リスト名」のところにリストの変数名を入れる
plt.plot(list_total_grains) # 「リスト名」のところにリストの変数名を入れる
plt.show()
