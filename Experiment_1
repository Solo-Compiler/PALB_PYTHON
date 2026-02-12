
# Question 1: Reverse the given array in place
class ReverseArray:
    def execute(self, sequence_values):
        left_index = 0
        right_index = len(sequence_values) - 1
        while left_index < right_index:
            sequence_values[left_index], sequence_values[right_index] = sequence_values[right_index], sequence_values[left_index]
            left_index += 1
            right_index -= 1
        return sequence_values


# Question 2: Find minimum and maximum element in array
class MinMaxFinder:
    def evaluate(self, dataset_values):
        smallest_value = dataset_values[0]
        largest_value = dataset_values[0]
        for element_value in dataset_values:
            if element_value < smallest_value:
                smallest_value = element_value
            if element_value > largest_value:
                largest_value = element_value
        return [smallest_value, largest_value]


# Question 3: Find kth smallest element
class KthSmallestElement:
    def determine(self, collection_values, position_k):
        ordered_values = sorted(collection_values)
        return ordered_values[position_k - 1]


# Question 4: Union of two arrays (distinct elements only)
class ArrayUnion:
    def merge(self, first_group, second_group):
        unique_container = set()
        for value_one in first_group:
            unique_container.add(value_one)
        for value_two in second_group:
            unique_container.add(value_two)
        return list(unique_container)


# Question 5: Find largest element in array
class LargestElementFinder:
    def identify(self, input_series):
        maximum_element = input_series[0]
        for entry_value in input_series:
            if entry_value > maximum_element:
                maximum_element = entry_value
        return maximum_element


# Question 6: Rotate array clockwise by one position
class ClockwiseRotation:
    def rotate_once(self, rotating_series):
        if len(rotating_series) <= 1:
            return rotating_series
        last_element_value = rotating_series[-1]
        for shift_index in range(len(rotating_series) - 1, 0, -1):
            rotating_series[shift_index] = rotating_series[shift_index - 1]
        rotating_series[0] = last_element_value
        return rotating_series


# Question 7: Maximum sum subarray (Kadane’s Algorithm)
class MaximumSubarraySum:
    def compute(self, numeric_stream):
        running_sum = numeric_stream[0]
        global_best = numeric_stream[0]
        for stream_index in range(1, len(numeric_stream)):
            running_sum = max(numeric_stream[stream_index], running_sum + numeric_stream[stream_index])
            global_best = max(global_best, running_sum)
        return global_best


# Question 8: Search Insert Position (Binary Search)
class SearchInsertPosition:
    def locate(self, ordered_list, target_value):
        start_pointer = 0
        end_pointer = len(ordered_list) - 1
        while start_pointer <= end_pointer:
            midpoint = (start_pointer + end_pointer) // 2
            if ordered_list[midpoint] == target_value:
                return midpoint
            elif ordered_list[midpoint] < target_value:
                start_pointer = midpoint + 1
            else:
                end_pointer = midpoint - 1
        return start_pointer


# Question 9: Two Sum (Return indices)
class TwoSumSolver:
    def solve(self, number_series, required_total):
        index_map = {}
        for position_marker in range(len(number_series)):
            complement_value = required_total - number_series[position_marker]
            if complement_value in index_map:
                return [index_map[complement_value], position_marker]
            index_map[number_series[position_marker]] = position_marker


# Question 10: Minimum number of jumps to reach end
class MinimumJumpsCalculator:
    def calculate(self, jump_capacity_series):
        length_series = len(jump_capacity_series)
        if length_series <= 1:
            return 0
        if jump_capacity_series[0] == 0:
            return -1

        max_reachable = jump_capacity_series[0]
        step_limit = jump_capacity_series[0]
        jump_count = 1

        for traversal_index in range(1, length_series):
            if traversal_index == length_series - 1:
                return jump_count

            max_reachable = max(max_reachable, traversal_index + jump_capacity_series[traversal_index])
            step_limit -= 1

            if step_limit == 0:
                jump_count += 1
                if traversal_index >= max_reachable:
                    return -1
                step_limit = max_reachable - traversal_index

        return -1
