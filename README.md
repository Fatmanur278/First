import math
# Nokta tanımı
points = [(1, 2), (3, 4), (5, 6), (7, 8)]
# Öklid mesafe fonksiyonu
def euclideanDistance(point1, point2):
    return math.sqrt((point2[0] - point1[0])**2 + (point2[1] - point1[1])**2)
# Mesafe hesapla
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)
# Minimum mesafe bul
min_distance = min(distances)
print(f"Minimum Öklid Mesafesi: {min_distance}")
