library(qcc)
# Cpk analysis for Machine 1 (Full Data)
process.capability(qcc_obj, spec.limits = c(45, 55), target = 50)
