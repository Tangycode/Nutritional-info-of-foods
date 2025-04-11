fooditems = {
    "Eggs":{"Carbs":1.1,"Protiens":12.6,"Fats":9.5},
    "Almonds":{"Carbs":21.6,"Protiens":21.2,"Fats":49.9},
    "Fish":{"Carbs":0,"Protiens":28,"Fats":15},
    "Cheese":{"Carbs":1.3,"Protiens":25,"Fats":33},
    "Peanuts":{"Carbs":16.1,"Protiens":25.8,"Fats":49.2},
}

def nutri_graph(name):
    data=fooditems[name]
    labels=data.keys()
    nutri=data.values()
    print(labels)
    print(nutri)
    plt.pie(nutri,labels=labels,autopct="%1.3f%%",startangle=120,
         wedgeprops={'edgecolor':'black','linewidth':1.5,'linestyle':'-'})
    plt.title(f"Nutritional info of {name}")
    plt.show()

name=input('Type of food name from the list: ')
nutri_graph(name)
