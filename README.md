# Ultimez_pythonfile
def calculate_pizza_slices(people):
    slices = {"Large": 8, "Medium": 6, "Regular": 4, "Small": 1}

    large_pizzas = people // slices["Large"]
    people %= slices["Large"]
    medium_pizzas = people // slices["Medium"]
    people %= slices["Medium"]
    regular_pizzas = people // slices["Regular"]
    people %= slices["Regular"]
    small_pizzas = people // slices["Small"]
    people %= slices["Small"]

    total_slices = (large_pizzas * slices["Large"]) + (medium_pizzas * slices["Medium"]) + (
            regular_pizzas * slices["Regular"]) + (small_pizzas * slices["Small"])

    return large_pizzas, medium_pizzas, regular_pizzas, small_pizzas, total_slices


people = int(input())
large, medium, regular, small, total_slices = calculate_pizza_slices(people)
print(f"If there are {people} individuals:")
print(f"1. {large} Large pizza")
print(f"2. {medium} Medium pizza")
print(f"3. {regular} Regular pizza")
print(f"4. {small} Small pizza")
print(f"Total slices needed: {total_slices}")

