def find_pairs(numbers, target):
    pairs = []
    seen = set()

    for number in numbers:
        complement = target - number

        if complement in seen:
            pairs.append((complement, number))

        seen.add(number)

    return pairs


if __name__ == "__main__":
    values = [2, 7, 4, 5, 3, 8, 1]
    target = 9

    print("Values:", values)
    print("Target:", target)
    print("Pairs:", find_pairs(values, target))
