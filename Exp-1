age_intervals <- c("1-5", "5-15", "15-20", "20-50", "50-80", "80-110")

frequencies <- c(200, 450, 300, 1500, 700, 44)



cumulative_frequencies <- cumsum(frequencies)

total_frequency <- sum(frequencies)

median_cf <- total_frequency / 2



median_interval_index <- which(cumulative_frequencies >= median_cf)[1]

median_interval <- strsplit(age_intervals[median_interval_index], "-")[[1]]



median_interval_width <- as.numeric(median_interval[2]) - as.numeric(median_interval[1])

median_cumulative_frequency_before <- cumulative_frequencies[median_interval_index - 1]

median_frequency_within_interval <- frequencies[median_interval_index]



median <- as.numeric(median_interval[1]) + ((median_cf - median_cumulative_frequency_before) / median_frequency_within_interval) * median_interval_width



print(paste("Approximate median value:", median))
